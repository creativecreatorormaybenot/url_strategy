# url_strategy [![Pub version](https://img.shields.io/pub/v/url_strategy.svg)](https://pub.dev/packages/url_strategy)

Package for Flutter apps that allows setting the web URL strategy with a single line of code.

## Usage

With a simple call of `setPathUrlStrategy`, your Flutter web app does not have a leading `#`
in the URL anymore 🚀

```dart
import 'package:url_strategy/url_strategy.dart';

void main() {
  // Here we set the URL strategy for our web app.
  // It is safe to call this function when running on mobile or desktop as well.
  setPathUrlStrategy();
  runApp(MyApp());
}
```

See the [`url_strategy` package README](https://github.com/simpleclub/url_strategy/tree/master/url_strategy)
or the [explanation on StackOverflow](https://stackoverflow.com/a/65709246/6509751) for more detailed usage documentation.

## Implementation

The package is basically a wrapper around the [`flutter_web_plugins`](https://github.com/flutter/flutter/tree/master/packages/flutter_web_plugins)
`setUrlStrategy`. The reason it exists is that using the function from `flutter_web_plugins`
requires conditional imports.  
The problem is solved by using a conditional export from the `url_strategy` package.
