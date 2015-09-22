# Getting Started

## CONTENTS

- [Manual Integration](#s1)

- [Using Cocoapods](#s2)

- [Using Carthage](#s3)

- [Initializing MagicVision in your app](#s4)

- [Start using MagicVision](#s5)

- [Troubleshooting](#s6)


## <span id = "s1">Manual Integration</span>

You can integrate the MagicVision SDK manually by follow the integration guide here.

### **Step 1:** Get the latest stable MagicVision SDK for iOS


[Get Magic Vision](https://github.com/GetMagicVision/MagicVision-iOS-SDK)


### **Step 2:** Adding the latest stable release of the SDK to your project

- Unzip the sdk & drag-drop `MagicVision.framework`, `Alamofire.framwwork` into your project folder.
- Add the the frameworks to `Link Binary With Libraries`


## <span id = "s2">Using Cocoapods</span>

If you are using [Cocoapods](http://cocoapods.org), you can integrate MagicVision with your iOS app by adding one line in the Podfile

- **Step 1:** Edit your cocoapods Podfile and add the line `pod 'MagicVision'` to get the latest SDK version available on Cocoapods. For a specific version use `pod 'MagicVision', '~> <version>'`. For example `pod 'MagicVision', '~> 0.0.1'`

- **Step 2:** Run `pod install` or `pod update` to refresh cocoapods dependencies


## <span id = "s3">Using Carthage</span>

If you are using [Carthage](https://github.com/carthage/carthage), you can integrate MagicVision with your iOS app by adding one line in the Cartfile

- **Step 1:** Edit your carthage Cartfile and add the line `github "GetMagicVision/MagicVision-iOS-SDK"` to get the latest SDK version available on Carthage. For a specific version use `github "GetMagicVision/MagicVision-iOS-SDK" ~> <version>`. For example `github "GetMagicVision/MagicVision-iOS-SDK" ~> 0.0.1`

- **Step 2:** Run `carthage update` to refresh cocoapods dependencies


## <span id = "s4">Initializing MagicVision in your app</span>

MagicVision can be used to support all the apps you publish. We uniquely identify each app that is registered with MagicVision using the combination of:

- *App Key*:This is your unique developer App Key

- *Secret Key*: This is your unique developer App Secret Key

To get the *App Key*, *Secret Key*, navigate to Settings>SDK (for Developers) in your agent dashboard and scroll down to “Initializing MagicVision section.

Select your App from the dropdown and copy the two tokens to be passed when initializing MagicVision.

Initialize MagicVision by calling the install method inside the application delegate method (ideally at the top):

```

#import "MagicVision"

...

func application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool {
    ...

    MagicVision.start("YOUR_APP_KEY", secretKey: "YOUR_SECRET_KEY")

    ...

    return YES;
}

```


## <span id = "s5">Start using MagicVision</span>

MagicVision is now integrated in your app. You should now use the support APIs to [detect face]() inside your app.

Run your app, and try starting a test using the API call.

Sample usage for detect face APIs:

```
let image: UIImage = ...
let face = FaceDetector.detectFace(image)
print("face x \(face.origin.x) y \(face.origin.y) width \(face.width) height \(face.height)")

```

## <span id = "s6">Troubleshooting</span>

If you are having issues with MagicVision integration, head over to the [Troubleshooting]() section for further information.
