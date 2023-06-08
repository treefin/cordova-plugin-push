# Cordova Plugin Push - Treefin Fork

[![Node CI](https://github.com/havesource/cordova-plugin-push/actions/workflows/ci.yml/badge.svg)](https://github.com/havesource/cordova-plugin-push/actions/workflows/ci.yml) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/422c67b5e70c4a0eadae7b9fc794d3c1)](https://app.codacy.com/gh/havesource/cordova-plugin-push?utm_source=github.com&utm_medium=referral&utm_content=havesource/cordova-plugin-push&utm_campaign=Badge_Grade_Settings)

> Register and receive push notifications

# What is this?


### --------------------------------------------------------------------------------------------
### **Treefin specific informations**

This is a forked version of the originial plugin. The main change is the bump of the Kotlin version, **from 1.5.20 to 1.7.10**. 

This change requires an additional update of the FCM version (FireBaseMessaging). This is done via the **add_platforms_plugins.sh** script in the **app** project. The original version of the FCM was 17.6.0, but is now set to 23.0.5.

### --------------------------------------------------------------------------------------------

This plugin offers support to receive and handle native push notifications with a **single unified API**.

This does not mean you will be able to send a single push message and have it arrive on devices running different operating systems. By default Android uses FCM and iOS uses APNS and their payloads are significantly different. Even if you are using FCM for both Android and iOS there are differences in the payload required for the plugin to work correctly. For Android **always** put your push payload in the `data` section of the push notification. For more information on why that is the case read [Notification vs Data Payload](https://github.com/havesource/cordova-plugin-push/blob/master/docs/PAYLOAD.md#notification-vs-data-payloads). For iOS follow the regular [FCM documentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref).

This plugin does not provide a way to determine which platform you are running on. The best way to do that is use the `device.platform` property provided by [cordova-plugin-device](https://github.com/apache/cordova-plugin-device).

* [Reporting Issues](docs/ISSUES.md)
* [Installation](docs/INSTALLATION.md)
* [API reference](docs/API.md)
* [Typescript support](docs/TYPESCRIPT.md)
* [Examples](docs/EXAMPLES.md)
* [Platform support](docs/PLATFORM_SUPPORT.md)
* [Cloud build support (PG Build, IntelXDK)](docs/PHONEGAP_BUILD.md)
* [Push notification payload details](docs/PAYLOAD.md)
* [Contributing](.github/CONTRIBUTING.md)
* [License (MIT)](MIT-LICENSE)

# Do you like tutorial? You get tutorial!

* [PhoneGap Day US Push Workshop 2016 (using node-gcm)](http://macdonst.github.io/push-workshop/)
