# Developer setup

Moved from the original project how-to. Web and Android steps assume you are on Windows unless noted.

## Website

1. Clone or pull the latest update from the repository
2. Open the project in your preferred IDE
3. `cd kalima-platform`
4. `npm install`
5. `npm start` for default website development
6. `npm run build` for production

## Testing for Android

1. Download Android Studio and install
2. Download Java JDK 21 from oracle.com
3. Configure environment variables for `%ANDROID_HOME%` and `%JAVA_HOME%`
4. `npm run build`
5. `npx cap sync`
6. `npx cap run android`

## How to configure environment variables

1. After installing Android Studio, go to search bar and type "environment variables"
2. Click on "Edit the system environment variables"
3. Click on "Environment Variables"
4. Click on "New"
5. Type `ANDROID_HOME` in the "Variable name" field and `C:\Users\<username>\AppData\Local\Android\Sdk` in the "Variable value" field, with username being your device username
6. Click on "New"
7. Type `JAVA_HOME` in the "Variable name" field and `C:\Program Files\Java\jdk-21` in the "Variable value" field
8. Click on "OK"
9. Restart your IDE and terminal
10. In cmd prompt or PowerShell as admin, run the following commands:
    - `setx JAVA_HOME "C:\Program Files\Java\jdk-17"`
    - `setx PATH "%PATH%;%JAVA_HOME%\bin"`
11. To verify, open cmd prompt as administrator and type `echo %ANDROID_HOME%` and `echo %JAVA_HOME%` — it should show you the locations of both variables
