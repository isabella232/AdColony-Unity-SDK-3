# AdColony SDK Unity Plugin
- Modified: May 25, 2018
- Unity Plugin Version: 3.3.4
- iOS SDK Version: 3.3.4
- Android SDK Version: 3.3.4

## Overview
AdColony delivers zero-buffering, [full-screen Instant-Play™ HD video](https://www.adcolony.com/technology/instant-play/), [interactive Aurora™ Video](https://www.adcolony.com/technology/auroravideo), and Aurora™ Playable ads that can be displayed anywhere within your application. Our advertising SDK is trusted by the world’s top gaming and non-gaming publishers, delivering them the highest monetization opportunities from brand and performance advertisers. AdColony’s SDK can monetize a wide range of ad formats including in-stream/pre-roll, out-stream/interstitial and V4VC™, a secure system for rewarding users of your app with virtual currency upon the completion of video and playable ads.

## Release Notes 3.3.4

* Updated to AdColony SDK 3.3.4 (iOS) and 3.3.4 (Android)
* [iOS] Fixed a bug where advertisement video's close button was not easily tappable because of the status bar overlapping.
* [iOS] Fixed a bug where unsafe access to the device's battery level was causing a crash mentioned in [iOS SDK issue #49](https://github.com/AdColony/AdColony-iOS-SDK-3/issues/49).
* [Android] Fixed new NullPointerException mentioned in [Android SDK issue #29](https://github.com/AdColony/AdColony-Android-SDK-3/issues/29#issuecomment-381380548).
* [Unity] Added a new API to pass user consent as required for compliance with the European Union's General Data Protection Regulation (GDPR). If you are collecting consent from your users, you can make use of this new API to inform AdColony and all downstream consumers of the consent. Please see our GDPR FAQ for more information and our GDPR wiki for implementation details.
* [Unity] Removed symbolic links from within native SDK
* [Unity] Fixed missing zone ID in some log statements
* [Unity] Fixed exception during OnRequestInterstitialFailed callback mentioned in [Unity Plugin issue #42](https://github.com/AdColony/AdColony-Unity-SDK-3/issues/42)
* [All] Several bug fixes and stability improvements.

See the full [release notes](https://github.com/AdColony/AdColony-Unity-SDK-3/blob/master/CHANGELOG.md) for more details.

## Getting Started

### Installation

1. In the Unity Editor, select "Assets"->"Import Package"->"Custom Package". Navigate to the location of the AdColony SDK Unity Plugin and select "AdColony.unitypackage".
1. Select "Import" to import all the assets into your project.
1. The AdColony SDK Unity Plugin includes Google's PlayServicesResolver to automatically pull in necessary Google Play Services libraries. If there are conflicts with this, the `play-services-ads` library is the only required. You can choose to ignore this PlayServicesResolver installation, remove the `AdColony/Editor/ADCDependencies.cs` file, and include the `play-services-ads` in another way.
1. The Plugins/Android/AdColony/AndroidManifest.xml file is automatically generated. To update manually, select "Tools"->"AdColony"->"Update AndroidManifest.xml".

See the full [Unity SDK integration documentation](https://github.com/AdColony/AdColony-Unity-SDK-3/wiki) for more details.

## Upgrade

#### From SDK 3.0:
In order to support thin/fat Android builds, we moved the native .so files from the `Plugins/Android/AdColony/libs` folder to the `Plugins/Android/libs` folder. Removing the `Plugins/Android/AdColony` folder before importing is recommended. Otherwise, simply remove the `Plugins/Android/AdColony/libs/armeabi-v7a` and `Plugins/Android/AdColony/libs/x86` folders.

#### From SDK 2.x:
Please note that updating from our 2.x Unity Plugin is not a drag and drop update, but rather includes breaking API and process changes. In order to take advantage of the 3.x Unity Plugin, a complete re-integration is necessary. Please review our [documentation](https://github.com/AdColony/AdColony-Unity-SDK-3/wiki) to get a better idea on what changes will be necessary in your app.


## Legal Requirements
By downloading the AdColony SDK, you are granted a limited, non-commercial license to use and review the SDK solely for evaluation purposes.  If you wish to integrate the SDK into any commercial applications, you must register an account with AdColony and accept the terms and conditions on the AdColony website.

Note that U.S. based companies will need to complete the W-9 form and send it to us before publisher payments can be issued.

## Contact Us
For more information, please visit AdColony.com. For questions or assistance, please email us at support@adcolony.com.
