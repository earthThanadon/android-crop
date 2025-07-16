## 1.0.5
* Resolved persistent build failures on JitPack.io caused by redundant and conflicting task dependency configurations. The explicit `dependsOn` for `publishReleasePublicationToMavenLocal` is now correctly positioned to ensure proper build order.

## 1.0.4
* Resolved JitPack.io Build Failures: Addressed the "implicit dependency" error by explicitly defining the build order between the AAR bundling and Maven publishing tasks. This ensures the library's .aar file is fully prepared before it's published.
* Enhanced Maven POM Metadata: Improved the Maven Publication configuration to correctly generate .pom metadata, including all necessary dependencies, ensuring a complete and valid published artifact.

## 1.0.3

* Package Name Refactor: The core package has been refactored from com.soundcloud.android.crop to com.earththanadon.androidcrop to establish clear ownership and prevent conflicts with the original archived library.
* JitPack.io Compatibility: Implemented necessary maven-publish plugin configurations in build.gradle to ensure successful builds and proper publication via JitPack.io.

## 1.0.2

* Gradle Upgrade: Updated Gradle to version 8.13 for improved build performance and compatibility with the latest Android Studio.
* Target SDK Update: Increased targetSdkVersion to 35, ensuring compatibility with the latest Android versions and security features.
* UI/UX Improvements: Implemented minor UI adjustments to better support Edge-to-Edge displays, providing a more immersive user experience.

## 1.0.1

* Support image picker helper from Fragments
* Restore support for SDK level 10
* Fix translucent status bar set via app theme
* Fix wrong result code when crop results in IOException
* Fix image "twitching" on zoom out to max bounds
* Translations: Italian, Turkish, Catalan, Swedish

## 1.0.0

* Improved builder interface: `Crop.of(in, out).start(activity)`
* Material styling
* Drop support for SDK level 9
* Start crop from support Fragment
* Fix max size
* Fix issue cropping images from Google Drive
* Optional circle crop guide
* Optional custom request code
* Translations: French, Korean, Chinese, Spanish, Japanese, Arabic, Portuguese, Indonesian, Russian

## 0.9.10

* Fix bug on some devices where image was displayed with 0 size

## 0.9.9

* Downscale source images that are too big to load
* Optional always show crop handles
* Fix shading outside crop area on some API levels
