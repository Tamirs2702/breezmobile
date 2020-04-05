# Breez Mobile Client

<p align='center'>
  <img src='https://breez.technology/prod/images/app/personal/2-66afa45814.png' height='300' alt='screenshot' />
  <img src='https://breez.technology/prod/images/app/personal/4-2e00fa09ab.png' height='300' alt='screenshot' />
  <img src='https://breez.technology/prod/images/app/personal/9-fb03a82c84.png' height='300' alt='screenshot' />
  <img src='https://breez.technology/prod/images/app/personal/8-4ba5326fc1.png' height='300' alt='screenshot' />
  <img src='https://breez.technology/prod/images/app/personal/10-a91670ec8d.png' height='300' alt='screenshot' />
</p>

[Breez](https://breez.technology) is a Lightning Network [mobile client](https://github.com/breez/breezmobile) and a [hub](https://github.com/breez/server). It provides a platform for simple, instantaneous bitcoin payments.

## Features

- [x] lnd on Android
- [x] Neutrino on Android
- [x] Seamless hub channel creation
- [x] Adding funds using on-chain tx
- [x] BTC & Satoshi units
- [x] Random avatars
- [x] Connect to Pay: simple interface to execute payments between users
- [x] Pay someone nearby: pay to another Breez user using NFC
- [x] NFC card support: activate an NFC card to be used by POS
- [x] A full lncli interface to query and execute ln commands
- [x] Filter tx by type
- [x] Filter tx by date
- [x] Pay invoice (link or QR) from other ln wallets
- [x] Create invoice (link or QR) to be paid by other ln wallets
- [x] Removing funds to an on-chain address
- [x] SubmarineSwaps for adding on-chain funds including refund functionality
- [x] End-to-end encryption of Connect-to-Pay session
- [x] Make Connect-to-Pay links work for users that didn't yet install Breez
- [x] Ability to Backup/Restore the ln node  
- [x] Mainnet support
- [x] Support zero-sat invoices
- [x] Startup optimizations
- [x] Background sync via FCM
- [x] Marketplace w/ Bitrefill
- [x] Adding funds via vouchers
- [x] Backup improvements
- [x] Add background ChannelsWatcher job
- [x] Expose Bitcoin Node (BIP157) configuration
- [x] iOS support
- [x] Add webLN support
- [x] Fiat units
- [x] Optional PIN
- [x] Adding funds via credit card
- [x] Add stronger encryption to cloud backup
- [x] iCloud backup option
- [x] Dark mode
- [x] Export payments to .csv
- [x] Support 3rd-party LSPs
- [x] Biometric login
- [x] Fast on-boarding
- [x] Pay w/o full sync
- [x] Implement lnurl-withdraw 
- [x] Send on-chain via reverse Submarine Swaps
- [x] Improve hodl invoice support
- [x] POS POC release
- [ ] Support zero-conf channels
- [ ] Async payments via Lightning Rod
- [ ] Support SD storage

## System Requirements
* Android 7+ 64bit

## Build
1. Build `breez.aar` and `bindings.framework` as decribed in https://github.com/breez/breez
2. For Android: 
- Copy `breez.aar` to the `android/app/libs/` directory
- Create a firebase Android app using the [firebase console](https://console.firebase.google.com/)
- Generate the google-services.json and copy it to the android/app/src/client directory
3. For iOS:
- Copy the bindings.framework directory to the ios directory.
- Create a firebase iOS app using the [firebase console](https://console.firebase.google.com/)
- Generate the GoogleServices-info.plist and copy it to ios/Runner directory
3. Flutter beta channel
- Install [flutter](https://flutter.dev/docs/get-started/install)
Run these command to switch to beta channel:
- flutter channel beta
- flutter upgrade
## Run
Now you can use the following commands to run in a connected device the client app or the pos or to build the corresponding apks:
 - flutter run --flavor=client --target=lib/main.dart
 - flutter run --flavor=pos    --target=lib/main_pos.dart
 - flutter build apk --target-platform=android-arm64 --flavor=client --debug   --target=lib/main.dart
 - flutter build apk --target-platform=android-arm64 --flavor=pos    --debug   --target=lib/main_pos.dart

## Architecture 
<p align='center'>
  <a href='https://breez.technology'>
    <img src='https://drive.google.com/uc?id=1s695NXHHlhfvtW1zdlntUzRloxhnBeg0&export=download' height='450' alt='screenshot' />
  </a>
</p>
