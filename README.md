# amplify_trips_planner

a flutter trip planner app for iOS and Android

## Getting Started

Build a Flutter Mobile App Using AWS Amplify

- [Hands-on AWS lab](https://aws.amazon.com/getting-started/hands-on/build-flutter-mobile-app-part-one/)

## Create an Amplify backend for the app

After cloning this repo, and opening the newly cloned Flutter app using VSCode.
You may do that by running the commands below in your terminal:

```
git clone https://github.com/ajlydi/amplify-trips-planner.git
cd amplify_trips_planner
code .
```

**Step 1:** Navigate to the app's root folder, and provision an Amplify backend for the app by running the following command in your terminal.

```
 amplify init
```

**Step 2:** Accept the auto-generated option for the environment name and choose the default editor. In this guide, we are using VSCode. Then select the AWS authentication method; we are using an AWS profile. Finally, choose the profile you want to use.

```
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the environment dev
? Choose your default editor: Visual Studio Code
Using default provider  awscloudformation
? Select the authentication method you want to use: AWS profile

For more information on AWS Profiles, see:
https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html

? Please choose the profile you want to use default
```

Press **Enter**. The Amplify CLI will initialize the backend and connect the project to the cloud. Once complete, you will get a confirmation and the Amplify CLI will add a new file `team-provider-info.json` to the `amplify` folder, which contains the Amplify backend details. It will also add a new dart file `amplifyconfiguration.dart` to the `lib/` folder. The app will use this file to know how to reach your provisioned backend resources at runtime.

**Step 3:** Run the following command to create the resources of the above categories in the cloud.

```
amplify push
```

**Step 4:** Press **Enter**. The Amplify CLI will deploy the resources and display a confirmation.


**Step 5:** Run the app in an emulator or simulator and try the following:
 
1. Create a new account
1. Create a new trip
1. Edit the newly created trip
1. Upload an image for the trip
1. Delete the trip
