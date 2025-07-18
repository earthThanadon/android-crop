> I guess people are just cropping out all the sadness

An Android library project that provides a simple image cropping `Activity`, based on code from AOSP.

## Features

* Gradle build & AAR
* Modern UI
* Backwards compatible to SDK 10
* Simple builder for configuration
* Example project

## Usage

First, declare `CropImageActivity` in your manifest file:

```xml
<activity android:name="com.earththanadon.android.crop.CropImageActivity" />
```

#### Crop

```java
Crop.of(inputUri, outputUri).asSquare().start(activity)
```

Listen for the result of the crop (see example project if you want to do some error handling):

```java
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent result) {
    if (requestCode == Crop.REQUEST_CROP && resultCode == RESULT_OK) {
        doSomethingWithCroppedImage(outputUri);
    }
}
```
    
Some attributes are provided to customise the crop screen. See the example project [theme](https://github.com/jdamcd/android-crop/blob/master/example/src/main/res/values/theme.xml).

#### Pick

The library provides a utility method to start an image picker:

```java
Crop.pickImage(activity)
```

## How does it look?

![android-crop screenshot](screenshot.png)

## License

This project is based on the [AOSP](https://source.android.com) camera image cropper via [android-cropimage](https://github.com/lvillani/android-cropimage).

    Copyright 2016 SoundCloud

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
