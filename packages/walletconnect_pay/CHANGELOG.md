## 1.1.0+vespr.1

VESPR fork of 1.1.0, consumed as a git dependency (`path: packages/walletconnect_pay`, `ref: 1.1.0+vespr.1`). Upstream PR: SPM support for walletconnect_pay (reown_flutter#396).

- iOS: Swift Package Manager support. The sources moved to `ios/walletconnect_pay/Sources/walletconnect_pay`, and `ios/walletconnect_pay/Package.swift` depends on the Yttrium Swift package 0.10.59, the same version as the podspec's YttriumWrapper. CocoaPods still works.
- iOS: the plugin's privacy manifest is bundled under both SPM and CocoaPods (the podspec had it commented out).
- The Dart and Android code is unchanged from 1.1.0, so `packageVersion` still reports `1.1.0`.

## 1.1.0

- Bump yttrium-wcpay to 0.10.60 (Android) / YttriumWrapper 0.10.59 (iOS).
- ConfirmPaymentRequest: new `data` field for wallet RPC results — elements may be plain strings or JSON objects (e.g. TRON's raw_data_hex + signature payload). `signatures` is deprecated and used as fallback when `data` is null.
- Fixed jniLibs pickFirsts to reference libuniffi_yttrium_wcpay.so.

## 1.0.2

- Sanitized quoted Windows OS version strings returned by WalletconnectPayUtils.getOS().

## 1.0.1

- Added WebView-based payment data collection
- Added per-option payment data collection
- Fixed WalletConnect Pay metadata handling
- Yttrium updates

## 1.0.0

- Official Flutter plugin for WalletConnect Pay

