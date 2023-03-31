# Flutter-Video-Player


1. Add the video_player dependency

This recipe depends on one Flutter plugin: video_player. First, add this dependency to your pubspec.yaml.

dependencies:
  flutter:
    sdk: flutter
  video_player:

2. Add permissions to your app

Next, update your android and ios configurations to ensure that your app has the correct permissions to stream videos from the internet.
Android

Add the following permission to the AndroidManifest.xml file just after the <application> definition. The AndroidManifest.xml file is found at <project root>/android/app/src/main/AndroidManifest.xml.

<manifest xmlns:android="http://schemas.android.com/apk/res/android">
    <application ...>

    </application>

    <uses-permission android:name="android.permission.INTERNET"/>
</manifest>

iOS

For iOS, add the following to the Info.plist file found at <project root>/ios/Runner/Info.plist.

<key>NSAppTransportSecurity</key>
<dict>
  <key>NSAllowsArbitraryLoads</key>
  <true/>
</dict>

