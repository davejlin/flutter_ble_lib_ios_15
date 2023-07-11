## 2.6.0

* Upgraded MultiPlatformBleAdapter dependency to a fork to support Android 12 and above

## 2.5.2

* Revert Android compileSdkVersion back to 30 as temporary fix for Android 12 incompatibilities

## 2.5.1

* Update Android compileSdkVersion to 31

## 2.5.0

* Update library to support Android V2 embedding
* Update example app to Android V2 embedding

## 2.4.3

* Assign transactionId a default value when rootObject["transactionId"] is null

## 2.4.2

* Change meta version to 1.3.0

## 2.4.1

* Use MultiplatformBleAdapter v0.1.9

## 2.4.0

* Add `BleManager#isClientCreated()` for checking whether native client exists


## 2.3.2

* Fix lack of disconnection event on iOS if connection failed to be established

## 2.3.1

* Fix connection timeout on iOS
* Fix emitting current connection state on iOS
* Update MBA to 0.1.7:
    * Fix lack of disconnection event on iOS when connection fails to be established
    * Fix not all errors being passed through onError callbacks on Android (thanks, @eliaslecomte)

## 2.3.0

* add `BleManager.createUnsafePeripheral()` to allow for connecting to known peripheral without launching scan first
  **NOTE:** this change will not work with BLEmulator below 1.2.0

## 2.2.9

* Fixed issue with incorrectly typed Stream

## 2.2.8

* Formatted all sources according to dartfmt for consistency

## 2.2.7

* Minor code style fixes. Adjusted device connection state monitoring.

## 2.2.6

* Fixed scan quick failures not being reported to the listener (race condition in scanning_mixin.dart)

## 2.2.5

* add missing handling of destroyClient call on iOS
* fix race condition in ConnectionStateStreamHandler (thanks, @cbreezier!)
* fix issue with picking incorrect characteristic on Android when there are multiple characteristics with the same UUID on the peripheral
* update pubspec format to properly display supported platforms
* fix messages in IllegalStateExceptions on Android

## 2.2.4

* Fix issue where `withResponse` argument was always true when writing to a characteristic on iOS
* Remove unnecessary file that was interfering with analyzer

## 2.2.3

* Fix issue with duplicated or malformed notification values

## 2.2.2

* Fix issue with invalid characteristic value base64 coding when performing characteristic operations on iOS
* Improve documentation

## 2.2.1

* Hide private APIs
* Add setup instructions to README
* Add missing descriptor operations information to README
* Moved permission_handler dependency to its place in example

## 2.2.0

* **NEW** operations on descriptors
* **BREAKING FOR BLEMULATOR** BLEmulator versions lower than 1.1.0 are not supported from this release
* Support for AndroidX
* Support for Swift 5
* Lower iOS deployment target to 8.0

## 2.1.0

* **BREAKING** ScanResult.AdvertisementData.ManufacturerData has changed type from Int8List to Uint8List
* Fix issue with invalid value of manufacturer data in scan results
* Fix issue with initialising plugin from a service without an active activity
* Update README with information about permissions
* Fix issue with default value of MTU when connecting to a peripheral on Android
* Fix issue where first few notifications right after start of monitoring a characteristic could get lost

## 2.0.1

* Fix issue with automatically generated transaction IDs.

## 2.0.0

* Dart 2.0 support
* **BREAKING** Completely new API. Consult [README](https://github.com/Polidea/FlutterBleLib/blob/master/README.md) for instructions on how to use the new version.
* Added [BLEmulator](https://github.com/Polidea/blemulator_flutter) support
