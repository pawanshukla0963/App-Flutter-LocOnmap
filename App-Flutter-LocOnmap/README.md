

# Flutter Map – Location plugin


A [flutter_map](https://pub.dev/packages/flutter_map) plugin to request and display the users location and heading on the map. The core features of the plugin are:

* Customization: The location button and marker can be completly customized.
* Energy efficiency: The location service is turned off if the app runs in the background.


## User experience

Status

* [x] The location button can be changed dependening on the location services status. For example also Google Maps shows a different icon if the location service is off.
* [x] The marker icon can be changed depending on the location accuracy.
* [x] It's possible to show the information (e.g. in form of a snackbar) to the user that the user location is outside of the map bounds.
* [x] The location heading is also shown for devices without an gyroscope. 

## Installation

Add flutter_map to your pubspec:

```yaml
dependencies:
  flutter_map_location: any # or the latest version on Pub
```

### Android

Ensure the following permissions are present in `<project-root>/android/app/src/main/AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
```



### iOS

Ensure the following permission is present in `<project-root>/ios/Runner/Info.plist`:

```xml
<key>NSLocationWhenInUseUsageDescription</key>
<string>App needs access to location and direction when open.</string>
```





## Demo / example

A working example can be found in the `example/` directory. It contains a page with the default settings:

![Default example](https://raw.githubusercontent.com/Xennis/flutter_map_location/main/example/default.png)

... and one with customized button and marker:

![Custom example](https://raw.githubusercontent.com/Xennis/flutter_map_location/main/example/custom.png)

(Map attribution: © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors)

## Credits

The plugin is inspired by [user_location_plugin](https://github.com/igaurab/user_location_plugin).