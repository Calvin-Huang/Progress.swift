# Progress.swift :hourglass: [![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage) [![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/jkandzi/Progress.swift/blob/master/LICENSE.txt)

Just wrap the `SequenceType` in your loop with the `Progress SequenceType` and you'll automatically get beautiful progress bars.

# Example

```swift
for i in 1...9 {
	...
}
```


```swift
for i in Progress(1...9) {
    ...
}
```


```
$ 4 of 9 [-------------                 ] ETA: 0:00:05 (at 1.01 it/s)
```

It also works with all the other types adopting the `CollectionType` protocol:

```swift
for i in Progress(["key": "value", "key2": "also value"]) {
    ...
}

for i in Progress([1, 52, 6, 26, 1]) {
    ...
}
```

```
$ 2 of 2 [------------------------------] ETA: 00:00:00 (at 1.00 it/s)
$ 3 of 5 [------------------            ] ETA: 00:00:02 (at 1.00 it/s)
```

#Installation
###Carthage

To integrate Progress.swift into your Xcode project using Carthage, specify it in your Cartfile:

```
github "jkandzi/Progress.swift"
```

Run `carthage update` to build the framework and drag the built `Progress.framework` into your Xcode project.

###Swift Package Manager

To install with the Swift Package Manager, add the following in your `Package.swift`:

```swift
import PackageDescription

let package = Package(
    name: "MyProject",
    dependencies: [
        .Package(url: "https://github.com/jkandzi/Progress.swift", majorVersion: 0)
    ]
)
```

###Manual

You can also copy the `Progress.swift` file into your Xcode project.

#Contribution

You are welcome to fork and submit pull requests.

#License

Progress.swift is released under the MIT license. See [LICENSE](https://github.com/jkandzi/Progress.swift/blob/master/LICENSE.txt) for details.
