# Genshin Automation

A great tool for traveler in Genshin Impact world!

This tool have:

- Automate get EXP for check in to the Hoyolab community and claim reward on Hoyolab site.

- Print your current info of the last 5 star gacha wish and current pity count.

- Export your gacha wish history from Genshin Impact account into Excel file and send it to Dropbox.

![Genshin Impact Daily Check-In rewards image](/images/hoyolab/hoyolab-reward-list.PNG)

## How to use this tool?

Fork this repository and you can go to the next step.

## Hoyolab Automation Setup

1. Please use Chrome browser so we are in same page. 🙏

2. Go to https://www.hoyolab.com/genshin/ then login

3. Right click on the page and clik Inspect element then go to **Console** tab. Then type `document.cookie` in **Console field** then press enter. It will show the value with format:
`mi18nLang=en-us; _ga=GAX.X.XXXXXXXXXX.XXXXXXXXXX; _MHYUUID=XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX; account_id=XXXXXXXX; cookie_token=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX; ltoken=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX; ltuid=XXXXXXXX; _gid=GAX.X.XXXXXXXXXX.XXXXXXXXXX`. Copy that!

Here's illustrated image for step 3.

![Hoyolab step 1](/images/hoyolab/h-step-1.png)

4. Go to **Secret menu in your fork repository** and make secret name **HOYOLAB_COOKIE** and paste the value you get from step 3.

Here are illustrated image for step 4.

![Wishxporter step 4](/images/wishxporter-img/w-step-5.png)

![Wishxporter step 5](/images/wishxporter-img/w-step-6.png)

5. Go to **Actions** menu in Workflows section click **Hoyolab Automation**. Click **Run workflow**, use **Branch: main** and click **Run workflow**.

![Hoyolab step 2](/images/hoyolab/h-step-4.png)


## Wishxporter Lite Setup

1. Get authkey url and set the url to **Secrets menu in your fork repository with name AUTHKEY_URL**. How to get it? Please see: [Get Authkey - Wishxporter](https://github.com/satyakresna/wishxporter/blob/main/README.en-US.md#get-authkey) for more info.

Here are illustrated image for step 1

![Wishxporter step 1.a](/images/wishxporter-img/w-step-5.png)

![Wishxporter step 1.b](/images/wishxporter-img/w-step-6.png)

2. Go to **Actions** menu in Workflows section click **Run Wishxporter Lite Mode**. Click **Run workflow**, use **Branch: main** and click **Run workflow**.

Here's illustrated image for step 2.

![Wishxporter step 2](/images/wishxporter-img/wishxporter-lite-mode-run-step.png)

3. Here's the result ater run step 2.

![Wishxporter step 3](/images/wishxporter-img/wishxporter-lite-mode-result.png)

**Note**: This workflow is manual trigger. So, you must repeat those steps above.


## Wishxporter Setup

1. Create application in [Dropbox App Console](https://www.dropbox.com/developers/apps).

2. Click **Scoped access**.

3. Choose **App folder** so the service will access to single folder created specially for your app.

4. Give the name for your app e.g **Wishxporter**

5. Click **Create App**

Here's illustrated image from step 2 to 5.

![Wishxporter step 1](/images/wishxporter-img/w-step-1.png)

6. Set permissions **files.content.write** in **Permissions tab** then click **Submit**.

Here's illustrated image for step 6.

![Wishxporter step 2](/images/wishxporter-img/w-step-2.png)

7. **Get access token** by click **Generate** with no expiration option in **Settings tab**. Copy the access token and we will use for the next step.

Here's illustrated image for step 7.

![Wishxporter step 3](/images/wishxporter-img/w-step-4.png)

8. Create secrets with name with name **DROPBOX_TOKEN** in **Secrets menu in your fork GitHub repository** and store the access token value there then click **Add secret**.

Here are illustrated image for step 8.

![Wishxporter step 4](/images/wishxporter-img/w-step-5.png)

![Wishxporter step 5](/images/wishxporter-img/w-step-6.png)

9. Get authkey url and set the url to **Secrets menu in your fork repository with name AUTHKEY_URL**. How to get it? Please see: [Get Authkey - Wishxporter](https://github.com/satyakresna/wishxporter/blob/main/README.en-US.md#get-authkey) for more info.

Here are illustrated image for step 9 (It's same with step 8).

![Wishxporter step 4](/images/wishxporter-img/w-step-5.png)

![Wishxporter step 5](/images/wishxporter-img/w-step-6.png)

10. Go to **Actions** menu in Workflows section click **Run Wishxporter**. Click **Run workflow**, use **Branch: main** and click **Run workflow**.

Here's illustrated image for step 10.

![Wishxporter step 6](/images/wishxporter-img/w-step-7.png)

**Note**: This workflow is manual trigger. So, you must repeat those steps above **if you want to get new history gacha data in Excel**.


## Closing

I hope this tool helps you and if you want to support please treat me on [trakteer.id/satyakresna](https://trakteer.id/satyakresna)
