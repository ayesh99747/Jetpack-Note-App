# JetpackNoteApp: A Simple Note-Taking Android App

This Android application provides a basic interface for creating and managing notes.  It utilizes Jetpack Compose for the UI and does not currently persist data beyond the app's lifecycle. This project was created following a course from O'Reilly Learning.

## Key Features

*   Create new notes with titles and descriptions.
*   View a list of existing notes.
*   Delete existing notes.
*   Simple and intuitive user interface built with Jetpack Compose.

## Technologies Used

*   **Kotlin:** The primary programming language.
*   **Jetpack Compose:**  Android's modern toolkit for building native UI.
*   **Android SDK (API 34):**  The Android software development kit.
*   **Gradle:** The build system.

## Prerequisites

*   **Android Studio:**  Required for building and running the application.  [Download Android Studio](https://developer.android.com/studio)
*   **Java Development Kit (JDK):** Ensure a compatible JDK is installed.  Android Studio will usually handle this for you.
*   **Android Emulator (or physical device):**  To run the app.

## Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    ```

2.  **Open the project in Android Studio:** Open the cloned `JetpackNoteApp` directory in Android Studio.

3.  **Sync the project:** Android Studio will automatically sync the project with Gradle.  If it doesn't, click "Sync Project with Gradle Files" in the toolbar.

4.  **Install dependencies:** Android Studio will automatically download and install necessary dependencies. You can also manually run:

    ```bash
    ./gradlew app:dependencies  //On Linux/macOS
    gradlew app:dependencies  //On Windows
    ```

5.  **Run the app:**  Select an emulator or connect a physical Android device and click the "Run" button in Android Studio.


## Project Structure

The project follows a standard Android project structure:

```
JetpackNoteApp/
├── app/                          // Main application code
│   ├── src/
│   │   ├── main/                 // Main source code
│   │   │   ├── java/             // Java code (though Kotlin is primarily used)
│   │   │   │   └── com/example/jetpacknoteapp/...
│   │   │   └── res/              // Resources (layouts, images, etc.)
│   │   ├── androidTest/         // Android instrumentation tests
│   │   └── test/                // Unit tests
│   ├── build.gradle.kts          // Module-level Gradle file
│   └── ...
├── gradle/                       // Gradle wrapper files
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── settings.gradle.kts           // Project-level Gradle file
├── build.gradle.kts              // Top-level Gradle file
└── ...
```

Screenshots are located in the `Screenshots/` directory.

## Usage Examples

The app has a simple layout:

*   **Add a Note:** Enter a title and description, then click "Save".
*   **View Notes:** The list of saved notes will display below the input fields. Each note shows the title, description and creation date.
*   **Delete a Note:** Click on a note in the list to remove it.  A Toast message will confirm the deletion.


## Configuration

The `gradle.properties` file contains project-wide Gradle settings such as JVM arguments and AndroidX configuration. The `app/build.gradle.kts` file contains the module-specific configurations for the app.  No special environment variables need to be set beyond what's normally required by Android Studio and the Android SDK.


## Scripts

*   `gradlew` (Linux/macOS) and `gradlew.bat` (Windows): These are wrapper scripts that manage the Gradle build process.  They handle downloading and executing the correct Gradle version.


## License

### Disclaimer

This repository contains code created while following the course  
**"Android Jetpack Compose - Build Android Native UIs Fast"** by **Paulo Dichone**,  
available at: [O’Reilly Learning Platform](https://learning.oreilly.com/course/android-jetpack-compose/9781803237718/)

The content is intended for educational purposes only and closely follows the structure and lessons from the original course.

All rights to the course content and materials belong to **Paulo Dichone**.  
This repository is not affiliated with or endorsed by Paulo Dichone or O’Reilly.

If you are the content owner and would like this repository modified or removed, please contact me directly.

## Error Handling

The application includes basic error handling:

*   If you try to save a note without a title or description, nothing will happen. A Toast message is shown after a successful note addition.
*   Input validation prevents non alphanumeric characters in the title and description.


This README provides a comprehensive overview of the JetpackNoteApp project.  Remember that this app does not persist data.  Additional functionality would be needed to add data persistence (e.g., using Room, SQLite, or other persistence mechanisms).

## Screenshots

<p align="center">
<img src="Screenshots/Screenshot 1.png" width="300" height="550">
<br>
<em>Figure 1: Home screen of the app with some notes.</em>
</p>

<p align="center">
<img src="Screenshots/Screenshot 2.png" width="300" height="550">
<br>
<em>Figure 2: Adding a new note.</em>
</p>

<p align="center">
<img src="Screenshots/Screenshot 3.png" width="300" height="550">
<br>
<em>Figure 3: Screenshot of the app with new notes added.</em>
</p>
