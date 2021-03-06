# 6.7 Declare Intended Use of Protected Data Classes

## Details

To help maintain the privacy of user data, iOS 10 requires developers to declare an app’s intended use of protected data classes with a purpose string key in the app’s `Info.plist` file. If the purpose string key is not included, the app will exit when it tries to access the protected data.

## Remediation

For apps on iOS 10.0 or later, developers must statically declare the intent to access specific interfaces and protected data and include a corresponding purpose string in the app’s `Info.plist` file for the following keys:
* `NSBluetoothPeripheralUsageDescription`
* `NSCalendarsUsageDescription`
* `NSCameraUsageDescription`
* `NSContactsUsageDescription`
* `NSHealthShareUsageDescriptionNSHomeKitUsageDescription`
* `NSLocationAlwaysUsageDescription`
* `NSLocationWhenInUseUsageDescription`
* `NSMicrophoneUsageDescription`
* `NSMotionUsageDescription`
* `NSPhotoLibraryUsageDescription`
* `NSRemindersUsageDescription`
* `NSSiriUsageDescription`
* `NSSpeechRecognitionUsageDescription`
* `NSAppleMusicUsageDescription`

The stated purpose string will display in the user prompt requesting access to relevant peripherals. Without a purpose string, the app will exit.


## References

 * Apple documentation: [Cocoa Keys - Key Summary](https://developer.apple.com/library/content/documentation/General/Reference/InfoPlistKeyReference/Articles/CocoaKeys.html#//apple_ref/doc/uid/TP40009251-SW35)

## CWE/OWASP

 * OWASP Mobile Top 10: [M7 - Client Code Quality](https://www.owasp.org/index.php/Mobile_Top_10_2016-M7-Poor_Code_Quality)
 * CWE: [CWE-264: Permissions, Privileges, and Access Controls](http://cwe.mitre.org/data/definitions/264.html)
