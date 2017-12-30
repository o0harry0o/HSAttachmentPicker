# HSAttachmentPicker

[![CI Status](http://img.shields.io/travis/helpscouts/HSAttachmentPicker.svg?style=flat)](https://travis-ci.org/helpscout/HSAttachmentPicker)
[![Version](https://img.shields.io/cocoapods/v/HSAttachmentPicker.svg?style=flat)](http://cocoapods.org/pods/HSAttachmentPicker)
[![License](https://img.shields.io/cocoapods/l/HSAttachmentPicker.svg?style=flat)](http://cocoapods.org/pods/HSAttachmentPicker)
[![Platform](https://img.shields.io/cocoapods/p/HSAttachmentPicker.svg?style=flat)](http://cocoapods.org/pods/HSAttachmentPicker)

`HSAttachmentPicker` creates a `UIAlertConroller` as a menu to access file data from photos, the camera, and the document browser APIs available on iOS.

![menu](https://dha4w82d62smt.cloudfront.net/items/3g1Q1K3Y1K3R0B2T2M3T/Screen%20Shot%202017-12-29%20at%2011.30.48%20AM.png | width=100)

## Usage

You'll want to create a new `HSAttachmentPicker`, assign a delegate, and call `showAttachmentMenu`.

```objective-c
    menu = [[HSAttachmentPicker alloc] init];
    menu.delegate = self;
    [menu showAttachmentMenu];
```

It's important you class holds a reference to the `HSAttachmentPicker` so it doesn't get garbage collected.




## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

The example project only contains a simple delegate that logs the operations for demonstration purposes.

## Requirements

In order to use the photo and camera related features, the `NSPhotoLibraryUsageDescription` and `NSCameraUsageDescription` properties need to be set in your application's `Info.plist` file. Without these the menu items will be unavailable.

![Info.plist](http://c.hlp.sc/3y3B3I2V0k0X)

For access to the document picker, you'll need the entitlements for iCloud and iCloud Containers. This will throw an error message via the delegate on the 'Import file from' menu option otherwise.

![iCloud](http://c.hlp.sc/1f3c3J1Y3e1i)

## Installation

HSAttachmentPicker is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'HSAttachmentPicker'
```

## License

HSAttachmentPicker is available under the MIT license. See the LICENSE file for more info.
