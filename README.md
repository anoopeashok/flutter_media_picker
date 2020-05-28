# media_picker

Flutter plugin to get pictures and videos.
It allows you to select one or more images from gallery or camera, without needing to switch provider.
It also allows you to select both images and videos if you wish

## Getting Started

For help getting started with Flutter, view our online
[documentation](https://flutter.io/).

**This Plugin is under development. It works in IOS and Android**

Forked from [Flutter Medias Picker](https://github.com/lubritto/Flutter_Medias_Picker)

For help on editing plugin code, view the [documentation](https://flutter.io/platform-plugins/#edit-code).

You need to put these styles to plugin works

```sh
  <style name="LibAppTheme" parent="Theme.AppCompat.Light.NoActionBar">
      <!-- Customize your theme here. -->
      <item name="colorPrimary">@color/colorPrimary</item>
      <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
      <item name="colorAccent">@color/colorAccent</item>
      <item name="android:colorBackground">@android:color/background_light</item>
      <item name="android:windowBackground">@android:color/white</item>
  </style>

  <style name="PickerTabLayout" parent="Widget.Design.TabLayout">
      <item name="tabBackground">@color/colorPrimary</item>
      <item name="tabGravity">fill</item>
      <item name="tabMaxWidth">0dp</item>
  </style>

  <style name="SmoothCheckBoxStyle">
      <item name="color_checked">@color/checkbox_color</item>
      <item name="color_unchecked">@android:color/white</item>
      <item name="color_unchecked_stroke">@color/checkbox_unchecked_color</item>
      <item name="color_tick">@android:color/white</item>
  </style>
```

in manifest:

add ```<uses-permission android:name="android.permission.CAMERA"/>``` in proguard-rules.pro add:

```
# Glide
-keep public class * implements com.bumptech.glide.module.GlideModule
-keep class * extends com.bumptech.glide.module.AppGlideModule {
 <init>(...);
}
-keep public enum com.bumptech.glide.load.ImageHeaderParser$** {
  **[] $VALUES;
  public *;
}
-keep class com.bumptech.glide.load.data.ParcelFileDescriptorRewinder$InternalRewinder {
  *** rewind();
}

# Uncomment for DexGuard only
#-keepresourcexmlelements manifest/application/meta-data@value=GlideModule

```

and in your podfile

```sh
platform :ios, '9.0'
use_frameworks!
```
