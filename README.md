# Veracode BCA Builder
Shell script to generate the BCA package to scan an iOS app.

## Parameters
The script takes three parameters:
1. The path to the `xcodeproj` or `xcworkspace` file
2. The scheme
3. The output directory (if using script in a Jenkins build, this should be your Jenkins workspace so the Veracode plugin can be used to upload)

## Build Settings
The script calls `xcodebuild` with `-destination generic/platform=iOS`, `DEBUG_INFORMATION_FORMAT=dwarf-with-dsym`, and `ENABLE_BITCODE=YES`.
The scheme must have the archive build configuration set to Debug. (From Product > Scheme > Edit Scheme, click Archive.
For Build Configuration, select Debug.)
See here for the full Veracode build settings documentation: https://help.veracode.com/reader/4EKhlLSMHm5jC8P8j3XccQ/PJWz14TuPBwScC2EpJtB2Q



