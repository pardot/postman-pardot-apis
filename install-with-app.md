[Back to main page](Readme.md)

> Instructions updated for Postman desktop app v8

# Installing with the Postman Desktop App

This is the recommended installation option because it is the fastest to set up and doesn’t require changes on your Salesforce org.

- [Installing with the Postman Desktop App](#installing-with-the-postman-desktop-app)
  - [Install the Postman App](#install-the-postman-app)
    - [Fork the Collection](#fork-the-collection)
  - [Configure the Collection](#configure-the-collection)
  - [Authenticate with Salesforce](#authenticate-with-salesforce)
  - [Execute a Request](#execute-a-request)


## Install the Postman App

Download and install the Postman app from [this link](https://www.postman.com/downloads).


### Fork the Collection

1. In the Postman desktop app, click on the top search bar and type **Salesforce**.
1. Click **Salesforce Developers** under Teams.

    ![Searching for Salesforce screenshot](doc-gfx/app/search-salesforce.png)

1. Click the **Pardot APIs** tile.
1. Click **Fork**

    ![Fork button screenshot](doc-gfx/app/fork-button.png)

1. Enter a label for your fork (e.g.: “My fork”).
1. Select a workspace (the default “My Workspace” workspace is fine).
1. Click **Fork Collection**.


## Configure the Collection

Before you can complete these steps, you must have a configured connected app and a Pardot Business Unit. See [Getting Started](https://developer.salesforce.com/docs/marketing/pardot/guide/getting-started.html) for help with creating a connected app and finding your business unit ID.

1. Click **Pardot APIs**
1. Open the **Variables** tab.
2. Update the variables. See the collection documentation for help. 
3. Click **Save**.


## Authenticate with Salesforce

You must authenticate to access the APIs. Doing so grants you an access token that is valid for a certain duration.

Repeat this step whenever your access token expires.

1. Click **Salesforce APIs**
2. Open the **Authorization** tab. The authorization type should be set to OAuth 2.0.
3. Click **Get New Access Token**. This opens a browser tab with the Salesforce login screen.
4. Log in to your Salesforce org.
5. Click **Allow** to grant access to your org.
6. If your environment is correctly set up, you should see a success message and be redirected to the Postman app. Click **Use Token** when prompted.

If you're not automatically redirected, you may need to allow popups in your browser.

    <details><summary>Click here for instructions on how to authorize popups.</summary>
    <p>
    Note: these instructions are for Chrome but the steps should be similar with other browsers.

    1. Click the popup error in the address bar, choose to allow popups from Postman:

        ![Allow popup screenshot](doc-gfx/web/allow-popup.png)

    2. Refresh the page and allow the browser to open the Postman app:

        ![Open Postman app screenshot](doc-gfx/web/allow-open-app.png)
    </p>
    </details>

## Execute a Request

1. Expand the collection and select the `Campaigns > Query` request.
1. Click `Send`.

If your environment is correctly set up, you should see a `200 OK` status. This means that you have successfully authenticated with Salesforce and that you can now use the other collection’s requests.

![Authenticate screenshot](doc-gfx/app/status200.png)

See [additional documentation](README.md#additional-documentation) for more information on how to keep the collection up to date and work with multiple Salesforce orgs.


[Back to main page](README.md)