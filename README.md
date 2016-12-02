##Translation Tool Plugin Sample

With the translation tool, translating strings has become an intern's job (yes, as easy as making coffee!).
This sample application shows how to configure the project with the translation tool.
More specifically, this sample consists of the main app module, 2 application flavors, and a library module, all of which 
obtain translations from a single Google Sheets spreadsheet. 
The translation tool plugin jar is provided in the project root directory. Alternatively, the dependency can be obtained from nexus. 
See comments in the project build.gradle file.
To update the project with the translationtions, simply run the updateTranslations task in gradle.

The translations spreadsheet for this sample: https://docs.google.com/spreadsheets/d/1xDXS4efBQSPmGzyvG5dw2l2hzpw1PWnqQYLyvZQqfL0/edit#gid=0

Notes:
- The master translation should be present as a Google Sheets spreadsheet. 
- The spreadsheet should be shared publicly on the web as read only.
- The spreadsheet should be published to the web.
- A sperate worksheet should be created for each project module and/or flavor.
- The worksheet name should match the module name. In case of a flavor, append the flavor name to the module name.
- Each module should have the translation tool plugin added to it's build.gradle file if translations are needed.
- Specify the spreadsheetId parameter in the build.gradle file. This is available in the spreadsheet URL.
- Both the translation plugin and spreadsheetId block should be added below the android block in the build.gradle file.
- Strings which do not need translations should be kept in the strings.xml file.
- Import the translations with the updateTranslations gradle task. This must be performed manually. Commit the updated auto-translated-strings.xml files to your repo.