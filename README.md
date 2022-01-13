# api31Splash
Demo android API 31 splash screen with Nativescript

Android 12 introduces a new splashscreen paradigm, which is detailed [here](https://developer.android.com/guide/topics/ui/splash-screen).

A good writeup on this an a step by step guide is given [here](https://itnext.io/a-comprehensive-guide-to-android-12s-splash-screen-api-644609c811fa).

This repo contains an app created from the `Hello World` angular template, updated to use the `alpha` version of `@nativesript\android` and built with the `next` version of the NS cli. ( i.e. pre 8.2 versions).

The original splash screen is shown for API<31 phones and the new type of splash screen for API>=31 phones.

( Well it works on the emulators anyway).


Note: I don't see the splash screen on API 31 emulator when I do `ns run android`  but if you relaunch the app on the emulator you see it.

## Changes


### package.json

Change `@nativescript/android` version to `alpha`

### app.gradle

Change to sdk 31 and add splashscreen dependency.

### App_Resources/Android/src/main/res/values/colors.xml

New white color

### App_Resources/Android/src/main/res/values/styles.xml

* Change the LaunchScreenThemeBase parent to the Splash screen style
* Add transparent colors for the new splash screen elements ( so that the old splash screen will show )

## New Files

* `App_Resources/Android/src/main/res/values-v31/styles.xml`
  Set the new splash screen properties to point to an animated image
* `App_Resources/Android/src/main/res/drawable-nodpi/ns_anim.xml`
  The animated image to show on the new splash screen.