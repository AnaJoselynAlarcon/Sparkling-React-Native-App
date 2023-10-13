# Setting up the Development Environment for React Native in Windows (Targeting Android)

This guide will walk you through setting up the development environment for React Native on a Windows machine, with Android as the target operating system.

## System Requirements

The system used for this documentation is:

- **CPU**:

  - Intel(R) Core(TM) i5-10300H CPU @ 2.50GHz

  Base speed: 2.50 GHz
  Sockets: 1
  Cores: 4
  Logical processors: 8
  Virtualization: Enabled
  L1 cache: 256 KB
  L2 cache: 1.0 MB
  L3 cache: 8.0 MB

  Utilization 5%
  Speed 1.98 GHz
  Up time 0:01:36:17
  Processes 298
  Threads 4122
  Handles 139081

- **MEMORY**:

  - 16.0 GB

  Speed: 2933 MHz
  Slots used: 2 of 2
  Form factor: SODIMM
  Hardware reserved: 132 MB

  Available 7.1 GB
  Cached 7.1 GB
  Committed 15.7/21.9 GB
  Paged pool 717 MB
  Non-paged pool 548 MB
  In use (Compressed) 8.6 GB (471 MB)

- **Windows Version**: 11.

## Prerequisites

1. **Node.js and npm**: Make sure you have Node.js and npm installed. You can download and install them from the [official Node.js website](https://nodejs.org/).
2. **Android Studio**

## Installing Android Studio and Configuring Environment for React Native on Windows

These are the steps I followed to install Android Studio and configure the necessary environment variables for React Native development on a Windows machine.

## Step 1: Installing Android Studio

1. Download Android Studio from the [official website](https://developer.android.com/studio).
2. Run the downloaded executable file to start the installation process.

3. **Select Installation Type**:

   - Choose "Standard" installation.

4. **Choose Theme**:

   - Select between light or dark.

5. **Components Setup**: Make sure you have selected:

- `Android SDK`
- `Android SDK Platform`
- `Android Virtual Device`
- `Performance Intel`

6. **Choose Installation Location**:

   - Choose the installation location or use the default taking in account it will take some space.

7. **Accept License Agreement**: Select each of the licenses and mark "Accept".

8. **Completing the Installation**:
   - Click "Finish" to complete the installation.

## Step 2: Configuring Environment Variables

1. Open the Windows Control Panel.

2. Click on "User Accounts", then click "User Accounts" again.

3. Click on "Change my environment variables".

4. **Adding ANDROID_HOME**:

   - Click "New..." to create a new user variable.
   - Set the variable name as `ANDROID_HOME`.
   - Find the path to your Android SDK in Android Studio
     ![Finding the path in Android Studio Step 1](<Screenshot 2023-10-12 212643.png>)
     ![Finding the path in Android Studio Step 2](<Screenshot 2023-10-12 214302.png>)
     "Settings" dialog, under "Languages & Frameworks" → "Android SDK".
   - Set the variable value to the path of your Android SDK (e.g., `C:\Android\SDK`).

   5. In that same window, you'll see the **path** option, here you will:
      a) Click Edit
      b) Click Browse
      c) Find the previous path and select a folder inside called **platform tools**.
      d) Click ok until is done.

# Creating a new application 💥

You have successfully installed Android Studio and configured the necessary environment variables for React Native development on Windows.
Now **FINALLY** we'll move on creating a new React Native app!

- Open the command prompt
- Navigate to the path were you want your project to live

```bash
npx react-native@latest init nameOfYourProject
```

Once it has started you can open the code folder

- On Visual Studio Code open the folder of your project and
  **tadaaa!** :raised_hands: we're good to go to the next part!

# Run the project in an Android Device Simulator.

## Create a Virtual Device in Android Studio

1. **Open Android Studio**:

   - Launch Android Studio on your machine.

2. **Open the VD Manager**:

   - Click on the "More Options" below "Open" icon and select "Virtual Device Manager.

3. **AVD Manager Window**:

   - The AVD Manager window will open, displaying a list of your existing AVDs (if any). Click the "Create Virtual Device" button.

4. **Select a Hardware Profile**:
   - Choose Phone.
   - Select Pixel 7.
   - Select "R" on the system image options.
     -Click Finish
   - Rename it
   - Select Portrait.

**Virtual Device Created**:

- The AVD is now created and listed in the AVD Manager.

## Running the Virtual Device

1. **Start the Virtual Device**:

   - In the AVD Manager, select the AVD you created.
   - Click the "Play" button or the "Run" link.

2. **Wait for Startup**:
   - The virtual device will start, and the Android OS will load. This may take a few moments.

# Run Project in Android Studio

1. Open folder containing the project.
2. Select "Build" from the top tool bar.
   2.1 Wait! (this can take a bit of time)
3. Open the command prompt, navigate to the folder of the project and insert the command:

```bash
npx react-native start
```

## Conclusion

You have successfully created a React Native App using a Virtual Device in Android Studio, allowing you to emulate Android devices on your computer for app testing and development.

# Troubleshooting

In the case you encounter some problems or errors here are a list of resources you can refer to:

- React Native [official website](https://reactnative.dev/docs/environment-setup?guide=native).

- Medium [react-native-training](https://medium.com/react-native-training).

-Stack Overflow [react-native-error](https://stackoverflow.com/search?q=react+native+installation+error&s=ad4a4548-2710-4640-bb24-9b58ec8869c8).
