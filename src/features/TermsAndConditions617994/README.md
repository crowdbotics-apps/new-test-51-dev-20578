# Terms & Conditions Screen

The Terms and Conditions Screen is a React Native based screen that renders terms and conditions with a simple header.

## Installation

After you have added the screen module into your project, you will need to configure a few items by modifying the project files in the github repository. Please note to replace ####### with the numeric sequence for your screen (found in folder name under `/src/features`) and also that the @BluePrint tags for ImportInsertion and NavigationInsertion will be removed in future so placement is with other imports and inside the AppNavigator above other screens.

### Step 1: Add screen into your project screen navigation.

**/src/mainNavigator.js:**
**ADD** immediately below in the section labeled //@BlueprintImportInsertion:

`import TermsAndConditionsNavigator from '../features/TermsAndConditions#######/navigator';`

**ADD** immediately below in the section inside AppNavigator definition labeled //@BlueprintNavigationInsertion section:

`TermsAndConditions#######: { screen: TermsAndConditionsNavigator },`

### STEP 3: Add Terms screen into the sidemenu navigation.

**/src/config/installed_blueprints.js**
**ADD**
Make sure any screens that aren’t desired in the side menu are removed from the file.

In installed_blueprints.js you need to add objects for every screen that you want to show in the sidemenu/splash screen.
They have a specific format:

`{ name: 'TermsAndConditions#######', human_name: 'Terms & Conditions', access_route: 'TermsAndConditions#######'}`

**name:** doesn't matter much, its used as a unique key for the side menu and splash screens array of
buttons, it must be unique, that's the only requirement

**human_name:** is what will be displayed in actual app

**access_route:** must be the name of the key in your mainNavigator setup

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
