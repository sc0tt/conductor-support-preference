[![](https://jitpack.io/v/sc0tt/conductor-support-preference.svg)](https://jitpack.io/#sc0tt/conductor-support-preference)


Library to create preference screens using [Conductor](https://github.com/bluelinelabs/Conductor) controllers instead of fragments.

## Including the library

You can include this library in your project with [JitPack](https://jitpack.io).
In your root build.gradle:

```groovy
allprojects {
    repositories {
        /// ...
        maven { url 'https://jitpack.io' }
	}
}
```

In your module build.gradle:
```groovy
dependencies {
    /// ...
    // For androidx.preference:preference:1.1.1
    implementation 'com.github.sc0tt:conductor-support-preference:1.1.1'
}
```

## Usage

Create a class that inherits from `PreferenceController` and include your preferences in the `onCreatePreferences` method, 
either by inflating an xml with `addPreferencesFromResource` or manually creating them, though you will need to provide
a `ContextThemeWrapper` if you use the latter and want to have a material theme.

Finally, use `Router::pushController` to show your preference controller.
