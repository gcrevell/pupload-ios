# Pupload for iOS

SwiftUI app for the Pupload photo backup server (`gcrevell/pupload-server`). See the README for how to build and test a change.

## Things that are easy to get wrong

- The project uses a synchronized folder group, so files added under `Pupload/` are picked up without editing `project.pbxproj`.
- This repo is public. Keep personal domains, hostnames and team IDs out of it, which is why the bundle ID is `com.pupload.Pupload`.
- Don't set `DEVELOPMENT_TEAM` in the project. The team is picked in Xcode.
- It targets iOS 27.0, so it builds with both the release Xcode and Xcode-beta on this Mac. Raise `IPHONEOS_DEPLOYMENT_TARGET` only when an API needs it, and then the README's requirements too.
