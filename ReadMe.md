# BarterDEX App

Before starting make sure you have `marketmaker` daemon compiled and running on your machine.

You can find instructions to install `marketmaker` here:

https://github.com/SuperNETorg/komodo/wiki/Setting-up-Liquidity-Provider-(LP)-Node#installing-liquidity-provider-lp-node-on-ubuntudebian-system

### Setup
Once running, follow these steps:
```shell
git clone https://github.com/KomodoPlatform/BarterDEX.git
cd BarterDEX
git pull
git checkout v0.8
npm install
npm start
```

It will download "BarterDEX". Open "BarterDEX", and from there open "index.html" file in your web browser.

### Update
To update, follow these steps:
```shell
cd BarterDEX
git pull
git checkout v0.8
git pull
```

#### For end users

To build the production ready app, install `electron-packager` and `electron-prebuilt` packages from npm
```shell
sudo npm install electron-packager -g
sudo npm install electron-prebuilt -g
```


### Instructions to test
1. Start Komodo Native Wallet
2. Start Monaize Native Wallet
3. Wait for both Komodo and Monaize to sync 100%
4. Start BarterDEX
5. Select 'Monzie (MNZ) dICO' option at the login screen.
6. Login with `passphrase` (either pre-generated or make a new one).
7. Look for the KMD address and send KMDs to it. Once sent, it will start reflecting there in a minute.
8. Give the maximum price that you would like to pay for MNZ. Example: 0.15
9. Give the maximum amount of MNZ you would like to buy. Example: 19
10. Wait and watch the MNZ balance increasing as trades happen.

#### Report Issues
Please feel free to test and post any bugs or issues found here: https://github.com/KomodoPlatform/BarterDEX/issues

#### Testing Notes
If your wallet is encrypted, the app will not work with it. This feature will be made available in coming releases.


### **Build the App**
Refer to the original [electron-packager](https://github.com/electron-userland/electron-packager) repository for more detailed information.

##### Linux
Change directory to BarterDEX and execute the following command to build the Linux app
```shell
cd BarterDEX
electron-packager . --platform=linux --arch=x64 --icon=assets/icons/barterdex/128x128.png --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/win64 --ignore=assets/bin/osx --overwrite
```
change architecture build parameter to ```--arch=x32``` for 32 bit build

##### OSX
Change directory to BarterDEX and execute the following command to build the OSX app
```shell
cd BarterDEX
electron-packager . --platform=darwin --arch=x64 --icon=assets/icons/barterdex/barterdex.icns --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/win64 --ignore=assets/bin/linux64 --overwrite
```

##### Windows
Change directory to iguana and execute the following command to build the Windows app
```shell
dir iguana
electron-packager . --platform=win32 --arch=x64 --icon=assets/icons/barterdex/barterdex.ico --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/osx --ignore=assets/bin/linux64 --overwrite

# If generating 32bit desktop package
electron-packager . --platform=win32 --arch=ia32 --icon=assets/icons/barterdex/barterdex.ico --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/osx --ignore=assets/bin/linux64 --overwrite

# To build both x64 and x86 desktop package
electron-packager . --platform=win32 --arch=all --icon=assets/icons/barterdex/barterdex.ico --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/osx --ignore=assets/bin/linux64 --overwrite
```
change architecture build parameter to ```--arch=x64``` for 64 bit build



## Localization Instructions

BarterDEX follows langauge and country code list localization file names. Please use the following links to get more info on the standard codes for country and language codes:

https://datahub.io/core/language-codes

https://datahub.io/core/country-list



