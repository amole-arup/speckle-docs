# Speckle Manager

Speckle Manager is a desktop application that handles accounts and connectors on your machine. You need to add a Speckle account to your computer using Manager in order for the Connectors to use them to send and receive data from a Speckle Server.

::: tip IMPORTANT 🙌
This guide assumes you have access to a **Speckle Server**.
It might have been provided by your company, you might have deployed one locally, or you might be using our [free official server](https://speckle.systems/getstarted/).
:::

## Installation

Speckle Manager is available for both Windows and Mac.

Download the latest version of Speckle Manager:

- [Speckle Manager for Windows](https://speckle-releases.ams3.digitaloceanspaces.com/manager/SpeckleManager%20Setup.exe)
- [Speckle Manager for Mac](https://speckle-releases.ams3.digitaloceanspaces.com/manager/SpeckleManager%20Setup.dmg)

Manager for Windows will automatically update when an update is available, in Mac you have to manually install new versions.

![screenshot of the manager](../.vuepress/public/assets/manager.png)

## Adding Accounts

Once you have downloaded the Manager, you'll be able to easily add an account. All you need to do is head to the "Accounts" menu, click the "Add Account" button, and provide your server URL. This will open a browser window where you can log in or register an account on that server and authorise the Manager.

You can also add an account directly from Speckle Web.

![manager-add-accounts](https://user-images.githubusercontent.com/7717434/106609140-2c07ba80-655d-11eb-9728-d59b850ac9a2.gif)

## Installing Connectors

The Manager also shows you the currently available connectors and allows you to install or remove connectors from your machine. Head into the "Connectors" menu to see what connectors you have installed and which are available to download. You'll also be able to check which version of each connector you have and update a connector as new versions are released.

![manager-connectors](https://user-images.githubusercontent.com/7717434/106609134-2b6f2400-655d-11eb-8d2a-1730115e3bc7.gif)

## Adding Accounts manually

Using Speckle Manager to handle your accounts and connectors is the recommended way, but if you'd like to do without it a manual flow is also available.

To manually add an account you first need to [generate a token for your account](/dev/tokens-apps).

Then you can proceed to create a `.json` file in `%appdata%\Speckle\Accounts\` with the following data structure:

```json
{
  "token": "YOUR-TOKEN-HERE",
  "serverInfo": {
    "name": "Server Name",
    "company": "Company Name",
    "url": "https://YOUR-SERVE-URL-HERE"
  },
  "userInfo": {
    "id": "YOUR-USER-ID",
    "name": "First Last",
    "email": "firstlast@email.com"
  }
}
```
