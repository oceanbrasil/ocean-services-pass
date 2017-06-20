# Pass SDK

[![Latest Stable Version](https://img.shields.io/badge/version-1.2.2-green.svg)](http://developer.samsung.com/galaxy/pass)

> __Note:__ 

> We regret to inform you that the Pass SDK will no longer provide DEVICE_FINGERPRINT_UNIQUE_ID for Samsung mobile devices starting from the second half of this year. We will no longer be providing a list of indexes and unique IDs for each registered fingerprint. Therefore, you will not be able to distinguish which fingerprints are used to verify the user.

Pass SDK allows you to use fingerprint recognition features in your application. With Pass SDK, you can provide reinforced security, by identifying whether the current user is the actual owner of the device.

![Pass](http://developer.samsung.com/sd2_images/galaxy/content/sms_pass_03.jpg)

You can use the Pass SDK to:

- Request fingerprint recognition
- Cancel fingerprint recognition requests
- Verify whether the fingerprint of the current user matches the fingerprint registered on the device
- Register fingerprints through the Enroll screen
- Get the index of the identified fingerprint from the array of registered fingerprints
- Get a list of names or unique ID or indexes of registered fingerprints
- Set the index of the fingerprint for recognition requests
- Add a title for the user interface
- Add a logo icon for the user interface
- Set the transparency of elements outside the user interface
- Set whether the user interface is dismissed or not when touching elements outside it
- Broadcast actions when registered fingerprint is changed
- Get the guide for poor quality
- Set the button for the user interface
- Change the standby string for the user interface

__Requesting Fingerprint Recognition__

![Pass 2](http://developer.samsung.com/sd2_images/galaxy/content/sms_pass_04_151217.jpg)

You can use a default or customized user interface (UI) for fingerprint recognition. Pass SDK also provides fingerprint recognition without a UI.

The fingerprint recognition UI is available with or without a Password button. With the Password button, the user has the option of providing identification using a device password instead of a fingerprint. To verify if the device supports a Password button, you have to use the related API and test it first.

__Cancelling Fingerprint Recognition Requests__

When fingerprint recognition is requested, the fingerprint sensor waits for the user input to read a fingerprint. If no fingerprint is read within 20 seconds, the request is automatically cancelled. Your application can also cancel the request directly before the 20 seconds are up. If the fingerprint recognition process is not required, cancel the request to save the devices battery.

__Checking for Registered Fingerprints on the Device__

You can verify whether registered fingerprints exist on the device. If there are no registered fingerprints, you can register new fingerprints.

__Registering Fingerprints__

If there are no fingerprints registered in the device, you can use Pass to prompt the user to jump to the Enroll screen where a fingerprint can be registered.

__Getting the Index of the Identified Fingerprint__

If fingerprint recognition is successful, you can get the index of the identified fingerprint from an array of registered fingerprint.

__Getting a List of Indexes and Names of Registered Fingerprints__

You can get a list of registered fingerprints on the device including their indexes and names.

__Getting a List of Indexes and Unique IDs of Registered Fingerprints__

You can get a list of registered fingerprints on the device including their indexes and unique IDs.

__Setting a Specific Fingerprint for Recognition__

You can tell Pass to check against only one of the registered fingerprints by using its index. If you haven't specified any indexes or if this is set to 'null', the API automatically checks for a match against all registered fingerprints.

__Adding a Title on the UI__

You can add a custom title on the identification dialog.

__Adding a Logo Icon on the UI__

Pass allows you to set a logo. This logo would appear at the bottom left corner of the user interface.

__Setting the Transparency of Background Elements__

You can set a value that can make background elements transparent.

__Setting Dialog Behavior when Background Elements are touched__

If you choose to set this value to true, the user interface would close when a user touches background elements.

__Broadcast actions when registered fingerprint is changed.__

Samsung devices send broadcasts to apps when the registered fingerprint is changed. For example, if fingerprint is added or removed, and all fingerprints are removed, the broadcast receiver can get fingerprint broadcasts.

__Getting the guide for the poor quality__

If you fail the fingerprint recognition due to the poor quality, you can get guide for the reason.

__Setting the button for the user interface__

You can set the button that can connect your own menu after user interface close.

__Changing the standby string for the user interface__

You can set the own standby string on the identification dialog.

__Restrictions__

Pass SDK has the following restrictions:

- Requires devices with Android 4.2 Jelly Bean (API level 17) or above
- Requires Fingerprint sensor.


## Download

Add into gradle project level

``` Gradle
allprojects {
  repositories {
    ...
    maven { url "https://jitpack.io" }
  }
}
```

Add into app project level

``` Gradle
dependecies{
    compile 'com.github.oceanbrasil:samsung-services-pass:1.2.2'
}```

Copyright © 2010 - 2017 SAMSUNG All rights reserved.

Portions of this page are reproduced from work created and shared by the Android Open Source Project and used according to terms described in the [Creative Commons 2.5](https://creativecommons.org/licenses/by/2.5/) Attribution License.
