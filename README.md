Mirrors [libPusher](https://github.com/lukeredpath/libPusher) using [Rome](https://github.com/neonichu/Rome) to create a Carthage-compatible Xcode project.

### To install:

- Add `github "Autoc0diq/libPusher"` to your `Cartfile`.

### To update to a new version:

- Update the gems and pods:
```
$ bundle update
$ bundle exec pod update
```
- Remove the current shared scheme
```
$ rm -rf Pods/Pods.xcodeproj/xcshareddata
```
- Share the scheme that builds `libPusher.framework` in `Pods.xcodeproj`
- Archive the framework using Carthage:
```
$ carthage build --no-skip-current
$ carthage archive libPusher
```
- Create a new tag that matches the NSLogger version in `Podfile.lock`
- Create a GitHub release for the tag and upload `libPusher.framework.zip` as an attachment
