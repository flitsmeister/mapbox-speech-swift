# MaplibreSpeech.swift

A module for using the Mapbox Speech API specifically tuned for the [Mapbox Navigation SDK](https://www.mapbox.com/navigation/).

# Why have we forked

1. We wanted to upgrade the SDK from iOS 9.0 to 12.0.

# What have we changed

- Upgrade iOS version from 9.0 to 12.0.

## Getting started
If you are looking to include this inside your project, you have to follow the the following steps:

Specify the following dependency in your [Carthage](https://github.com/Carthage/Carthage) Cartfile:

```cartfile
github "mapbox/MapboxSpeech.swift" ~> 0.1
```

Or in your [CocoaPods](http://cocoapods.org/) Podfile:

```podspec
pod 'MapboxSpeech.swift', '~> 0.1'
```

Then `import MapboxSpeech` or `@import MapboxSpeech;`.

## Basic Usage

```swift
// main.swift
import MapboxSpeech

let voice = SpeechSynthesizer(accessToken: "Your Mapbox access token")
let options = SpeechOptions(text: "hello, my name is Bobby")

voice.audioData(with: options) { (data: Data?, error: NSError?) in
    // Do something with the audio!
}
```

Copyright (c) 2023 MapLibre contributors
