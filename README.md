# Pangle iOS SDK Beta

Pangle iOS SDK Beta package for Swift Package Manager.

## Integration

Before integrating the package, make sure the app target enables the `-ObjC` linker flag in Xcode: select the app target, open Build Settings, search for Other Linker Flags, and add `-ObjC`.

### Option 1: Add the package in Xcode

In Xcode, choose File -> Add Package Dependencies..., then enter:

```text
https://github.com/bytedance/AdsGlobalPackage-Beta.git
```

Select a Beta tag, for example:

```text
8.4.0-beta.0
```

Choose the product:

```text
AdsGlobalPackage
```

Import the SDK in code:

```swift
import AdsGlobalPackage
```

### Option 2: Add the package in Package.swift

Add the Beta package dependency:

```swift
dependencies: [
    .package(
        url: "https://github.com/bytedance/AdsGlobalPackage-Beta.git",
        exact: "8.4.0-beta.0"
    )
]
```

Then add the product dependency to your target:

```swift
targets: [
    .target(
        name: "YourTarget",
        dependencies: [
            .product(name: "AdsGlobalPackage", package: "AdsGlobalPackage-Beta")
        ]
    )
]
```

Import the SDK in code:

```swift
import AdsGlobalPackage
```
