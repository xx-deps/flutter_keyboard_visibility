# Flutter Keyboard Visibility Temp Fork

A fork of [flutter_keyboard_visibility_web](https://pub.dev/packages/flutter_keyboard_visibility_web) that's compatible with Flutter/WASM and [flutter_keyboard_visibility](https://pub.dev/packages/flutter_keyboard_visibility). This package is not used by [flutter_keyboard_visibility_temp_fork](https://pub.dev/packages/flutter_keyboard_visibility_temp_fork).

This is a temporary unofficial fork of [flutter_keyboard_visibility_web](https://pub.dev/packages/flutter_keyboard_visibility_web). Will be maintained for a short while once we find a replacement.

We don't recommend using this package as a dependency in packages published to [pub.dev](https://pub.dev/) as it's very likely to be break after a short while, however, if you're developing an app, this might be a temporary replacement if you want to build with [Flutter WebAssembly](https://docs.flutter.dev/platform-integration/web/wasm).

Unlike [flutter_keyboard_visibility_temp_fork](https://pub.dev/packages/flutter_keyboard_visibility_temp_fork), this is unpublished and made compatible with `flutter_keyboard_visibility`. If you're using dependencies that use `flutter_keyboard_visibility` as a transitive dependency, and you're unable to build with WASM, you can override the [flutter_keyboard_web](https://pub.dev/packages/flutter_keyboard_web) with this modified version:

```yaml
dependency_overrides:
  # The flutter_keyboard_visibility_web uses dart:html which is incompatible with WASM, override it with a modified version that uses the web package instead.
  flutter_keyboard_visibility_web:
    git:
      url: https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork.git
      ref: master
      path: flutter_keyboard_visibility_web
```

This package is compatible with `flutter_keyboard_visibility` since it holds the same name as `flutter_keyboard_visibility_web`, both are published packages and we're unable to publish this package.

> [!NOTE]
> The web implementation of `flutter_keyboard_visibility_temp_fork` is bundled within the same package. You only need this package if you're using a dependency that uses `flutter_keyboard_visibility_web` and you're unable to build with **Flutter/WASM**.

See [flutter_keyboard_visibility_temp_fork #3](https://github.com/EchoEllet/flutter_keyboard_visibility_temp_fork/pull/3) and [flutter_keyboard_visibility #155](https://github.com/MisterJimson/flutter_keyboard_visibility/pull/155) for more details.