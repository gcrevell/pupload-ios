# Pupload for iOS

The iPhone and iPad app for [Pupload](https://github.com/gcrevell/pupload-server), which backs up your iCloud photos to your own server. For now it's an empty SwiftUI app that shows "Hello, world!".

<img src="docs/hello-world.png" width="250" alt="Pupload showing Hello, world!">

## Requirements

- Xcode 27 or later
- An iPhone or iPad on iOS 27 or later
- An Apple ID signed in to Xcode. A free Personal Team is enough.

## Install on your iPhone

1. Open `Pupload.xcodeproj` in Xcode.
2. Select the **Pupload** target, open **Signing & Capabilities**, and pick your team under **Team**. If Xcode says the bundle ID is taken, change `com.pupload.Pupload` to something unique.
3. Connect your iPhone with a cable, or pair it over Wi-Fi in **Window › Devices and Simulators**, and select it as the run destination.
4. Press **⌘R**. The first time, iOS asks you to turn on **Developer Mode** (Settings › Privacy & Security › Developer Mode) and restart.

## Build and test a change

Build for the simulator from the command line:

```sh
xcodebuild -project Pupload.xcodeproj -scheme Pupload \
  -destination 'generic/platform=iOS Simulator' build
```

The build should finish with no warnings. Then run it from Xcode on an iPhone and an iPad simulator, and check that each screen you changed looks right on both.
