# Secure Cash Wallet Electron

This is a GUI wallet for Secure Cash made using Electron, this means it's written in JavaScript, HTML and CSS. 
It is meant to be able to work on Windows, Linux and MacOS, however so far I've only been able to test it on Windows.

As of now, this wallet contains the basic functions required to operate with Secure Cash, this includes:
  * Load a wallet file
  * Generate a new wallet container file
  * Import an existing wallet using keys
  * Show private keys
  * See balance and transactions
  * Send SCSX

There is still plenty of room for improvements and features, so I will gladly accept help from anyone who is capable of lending a hand. Right now the code is still in beta phase with some rough edges and should be polished in order to make a proper release.

### How to Use

Once you got Wallet-electron running (see the sections below), you will need to specify the path to walletd.exe in the Settings tab (the cog icon in the top left). Walletd comes with the Secure Cash .zip, and will not work with a versions below 0.3.1.

Now you can switch back to the Overview and click the 'Load Wallet' button to start using Wallet-electron. If you don't have a wallet file you can generate a new one with the 'Create Wallet' button or import one using your private keys with the 'Import Wallet' button.


### How to Build

You can build it manually following the [Application Distribution](https://electronjs.org/docs/tutorial/application-distribution) guide in the Electron documentation. 

However the easiest way I have tried so far is using a npm package called `electron-packager`. In order to do so you need to install it globally by typing `npm install electron-packager -g`. 

npm install

Now you can build Wallet-electron by typing:

electron-packager /'directory' --platform=win32 --arch=x64 --out=releases/ --app-version=0.0.1

Where `directory` is the path to your folder and `--out` is the path to the folder where the app is going to be generated.

Using that command will generate a build for the platform and architecture you are currently using. You can use the `--platform=<platform>` and `--arch=<arch>` optional flags if you want to build it for something else. You can check https://github.com/electron-userland/electron-packager for extra info regarding this tool.
