This repository hosts the [Serial Standard](https://serial.spec.whatwg.org/). It is one of [many web standards](https://spec.whatwg.org/) developed by the [WHATWG community](https://whatwg.org/).

## Code of conduct

We are committed to providing a friendly, safe, and welcoming environment for all. Please read and respect the [Code of Conduct](https://whatwg.org/code-of-conduct).

## Contribution opportunities

Folks notice minor and larger issues with the Serial Standard all the time and we'd love your help fixing those. Pull requests for typographical and grammar errors are also most welcome.

Issues labeled ["good first issue"](https://github.com/whatwg/serial/labels/good%20first%20issue) are a good place to get a taste for editing the Serial Standard. Note that we don't assign issues and there's no reason to ask for availability either, just provide a pull request.

If you are thinking of suggesting a new feature, read through the [FAQ](https://whatwg.org/faq) and [Working Mode](https://whatwg.org/working-mode) documents to get yourself familiarized with the process.

We'd be happy to help you with all of this [on Chat](https://whatwg.org/chat).

## Pull requests

In short, change `index.bs` and submit your patch, with a [good commit message](https://github.com/whatwg/meta/blob/main/COMMITTING.md).

Please add your name to the Acknowledgments section in your first pull request, even for trivial fixes. The names are sorted lexicographically.

To ensure your patch meets all the necessary requirements, please also see the [Contributor Guidelines](https://github.com/whatwg/meta/blob/main/CONTRIBUTING.md). Editors of the Serial Standard are expected to follow the [Maintainer Guidelines](https://github.com/whatwg/meta/blob/main/MAINTAINERS.md).

## Tests

Tests are an essential part of the standardization process and will need to be created or adjusted as changes to the standard are made. Tests for the Serial Standard can be found in the `serial/` directory of [`web-platform-tests/wpt`](https://github.com/web-platform-tests/wpt).

A dashboard showing the tests running against browser engines can be seen at [wpt.fyi/results/serial](https://wpt.fyi/results/serial).

## Building "locally"

For quick local iteration, run `make`; this will use a web service to build the standard, so that you don't have to install anything. See more in the [Contributor Guidelines](https://github.com/whatwg/meta/blob/main/CONTRIBUTING.md#building).

## Explainer

Details about the API including example usage code snippets and its motivation, privacy, and security considerations are described in [EXPLAINER.md](./EXPLAINER.md). Extensions to this API to support connections to Bluetooth RFCOMM services are described in [EXPLAINER_BL
UETOOTH.md](./EXPLAINER_BLUETOOTH.md).

## Implementation Status

This API has three implementations: [Blink](https://source.chromium.org/chromium/chromium/src/+/main:third_party/blink/renderer/modules/serial/), [Gecko](https://github.com/mozilla-firefox/firefox/tree/main/dom/webserial), and [a polyfill](https://github.com/google/web-serial-polyfill/).

The Blink implementation is available in browsers based on Chromium 89 and later, such as Google Chrome and Microsoft Edge. Individual Chromium-based browsers may choose to enable or disable this API. The initial release was limited to desktop OSes (Windows, macOS, Linux, and ChromeOS) however as of Chromium 148 this API is available on Android-based devices as well.

The Gecko implementation is available in browsers based on Firefox 151 and later on desktop OSes (Windows, macOS, and Linux).

The polyfill implementation is based on the WebUSB API and currently only supports standard USB communications class devices but could be expanded to support other proprietary USB to serial adapters. It could also be expanded to support Bluetooth Low Energy UARTs via the Web Bluetooth API.
