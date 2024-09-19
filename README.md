This is a starter repo for https://se-education.org/guides/tutorials/javaFx.html

# JavaFX Chatbot Project - Duke GUI

This project is a JavaFX-based chatbot application called Duke. It demonstrates how to build a GUI for a chatbot using JavaFX. The project follows a tutorial format and is split into several stages, from setting up the basic project structure to incorporating a fully functional GUI with FXML.

## Prerequisites

- **Java Development Kit (JDK) 17**: Ensure that you have JDK 17 installed on your system.
  - You can download it from [here](https://www.oracle.com/java/technologies/javase-jdk17-downloads.html).
  
- **Gradle**: Gradle is used for managing dependencies and building the project.
  - To install Gradle, refer to [Gradle installation guide](https://gradle.org/install/).

- **Integrated Development Environment (IDE)**: We recommend using IntelliJ IDEA, but any Java-supporting IDE should work.
  - For IntelliJ, refer to [IntelliJ IDEA Setup](https://www.jetbrains.com/idea/download/) and configure it with JDK 17.

## Setup Instructions

### Clone the Repository:
```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

### Open the Project in Your IDE:
If you're using IntelliJ IDEA, open the project from the main screen. Make sure to import the build.gradle file for Gradle setup.

### Configure JavaFX Dependencies:
Update your build.gradle file to include the following dependencies for JavaFX based on your operating system:

```bash
repositories {
    mavenCentral()
}

dependencies {
    String javaFxVersion = '17.0.7'

    implementation group: 'org.openjfx', name: 'javafx-base', version: javaFxVersion, classifier: 'win'
    implementation group: 'org.openjfx', name: 'javafx-base', version: javaFxVersion, classifier: 'mac'
    implementation group: 'org.openjfx', name: 'javafx-controls', version: javaFxVersion, classifier: 'win'
    implementation group: 'org.openjfx', name: 'javafx-controls', version: javaFxVersion, classifier: 'mac'
    implementation group: 'org.openjfx', name: 'javafx-fxml', version: javaFxVersion, classifier: 'win'
    implementation group: 'org.openjfx', name: 'javafx-fxml', version: javaFxVersion, classifier: 'mac'
    implementation group: 'org.openjfx', name: 'javafx-graphics', version: javaFxVersion, classifier: 'win'
    implementation group: 'org.openjfx', name: 'javafx-graphics', version: javaFxVersion, classifier: 'mac'
}
```

### Sync Dependencies:
- For IntelliJ IDEA: Use the Gradle tool window to refresh and reload dependencies.
- Without an IDE: Run the following command in the terminal:
```./gradlew clean build```

### Running the Project:
- Run the project using Gradle in the terminal:
```./gradlew run```
- Alternatively, use your IDE's run configuration to run the Launcher class.

### Setting Up FXML (Optional):
You can install Scene Builder to visually design the JavaFX GUI components and bind them to your controller classes.

## Development
The project structure contains:

- Main.java: Entry point for the JavaFX application.
- Launcher.java: Acts as the launcher to avoid classpath issues.
- MainWindow.fxml: FXML file that defines the GUI layout.
- DialogBox.java: Custom control for chat dialog boxes.

## Running the Application
After setting everything up, you should be able to run the application and see the following window:
- A simple GUI with a text input field, a send button, and a scrollable area for displaying the conversation.

## Troubleshooting
Common Issues
JavaFX not loading properly:

Ensure that you're using JDK 17 and the correct JavaFX version. Check the Gradle dependencies and reload them.
Unsupported JavaFX configuration warning:

This warning can be safely ignored if you are using a newer version of JavaFX with an older JDK.
FXML or resource loading issues:

Make sure that the paths in your code (e.g., image paths) are correct and relative to the resources directory.
Platform-Specific Notes
Windows
Ensure JavaFX libraries are properly set with the classifier win in your build.gradle.
macOS
Ensure JavaFX libraries are set with the classifier mac in your build.gradle.
License
This project is open-source and available under the MIT License.


<img width="421" alt="Screenshot 2024-09-06 at 11 31 24 AM" src="https://github.com/user-attachments/assets/b662c8a8-d753-4653-a0b0-413ceef961ef">
