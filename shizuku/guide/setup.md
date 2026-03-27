# User manual

[[toc]]

## Start Shizuku

Shizuku supports startup in the following three ways.

::: tip If you are using GrapheneOS

System settings - "Security" - "Secure app spawning" may need to be disabled.

[Source](https://git# About contributing to GitHub Docs

You can contribute to GitHub Docs content in several ways.

GitHub documentation is open source. Anyone can contribute to the docs in the public `docs` repository: <https://github.com/github/docs>. GitHub employees work on the documentation in a copy of this repository called `docs-internal`. The two repositories are automatically synced to keep them both up to date with changes merged into the `main` branch of either repository. For simplicity, we'll refer to "the documentation repository" in the articles about contributing to GitHub Docs.

The documentation repository is the place to discuss and collaborate on the documentation that is published here on [docs.github.com](/en).<!-- markdownlint-disable-line search-replace -->

## Issues

[Issues](/en/github/managing-your-work-on-github/about-issues) are used to track tasks that contributors can help with. If an issue has a `triage` label, we haven't reviewed it yet, and you shouldn't begin work on it.

If you've found something in the documentation content, or something about the docs.github.com website, that should be updated, search the open issues to see if someone else has reported the same thing. If it's something new, open an issue using a [template](https://github.com/github/docs/issues/new/choose). We'll use the issue to have a conversation about the problem you'd like to be fixed.<!-- markdownlint-disable-line search-replace -->

> \[!NOTE]
> GitHub employees should open issues in the private `docs-content` repository.

## Pull requests

A [pull request](/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) is a way to suggest changes in our repository. When we merge those changes, they're deployed to the live site within 24 hours.

We cannot accept contributions to the [REST API reference documentation](/en/rest/reference). If you spot an inaccuracy in the REST API reference documentation, open an issue in the [`rest-api-description`](https://github.com/github/rest-api-description/issues/new?template=schema-inaccuracy.md) repository.

We only document GitHub products, features, tools, and extensions. We may mention or link to third-party tools to demonstrate how a feature works, but we do not accept pull requests to document third-party tools or integrations unless they were codeveloped with GitHub.

### Reviewing your own pull requests

You should always review your own pull request first, before marking it as ready for review by others.

For content changes, make sure that you:

* Confirm that the changes meet the user experience and goals outlined in the content design plan (if there is one).
* Review the content for technical accuracy.
* Check your changes for grammar, spelling, and adherence to the [Style guide](/en/contributing/style-guide-and-content-model/style-guide).
* Make sure the text in your pull request will be easy to translate. For more information, see [Writing content to be translated](/en/contributing/writing-for-github-docs/writing-content-to-be-translated).
* Check new or updated Liquid statements to confirm that versioning is correct. For more information, see [Versioning documentation](/en/contributing/syntax-and-versioning-for-github-docs/versioning-documentation).
* Check the preview of any pages you have changed. A preview is automatically generated after you submit a pull request and links are added to the pull request. The preview sometimes takes several minutes before it is ready to view. Confirm that everything is rendering as expected. Checking the preview will help you identify problems such as typos, content that doesn't follow the style guide, or content that isn't rendering due to versioning problems. Make sure to check the rendered output for lists and tables, which can sometimes have problems that are difficult to identify in the Markdown.
* If there are any failing checks in your pull request, troubleshoot them until they're all passing.

## Support

We are a small team working hard to keep up with the documentation demands of a continuously changing product. Unfortunately, we just can't help with support questions in this repository. If you are experiencing a problem with GitHub, unrelated to our documentation, please [contact GitHub Support directly](https://support.github.com/contact). Any issues or pull requests opened in the documentation repository requesting support will be given information about how to contact GitHub Support, then closed and locked.

If you're having trouble with your GitHub account, contact [Support](https://support.github.com/contact?tags=docs-contributing-guide).

## Translations

This website is internationalized and available in multiple languages. The source content in this repository is written in English. We automate translations through an internal process, working with professional translators to localize the English content.

If you spot a translation error, please raise an issue with the details.

We do not currently accept pull requests for translated content.

## Site policy

GitHub's site policies are also published on docs.github.com.<!-- markdownlint-disable-line search-replace -->

If you find a typo in the site policy section, you can open a pull request to fix it. For anything else, see [Contributing](https://github.com/github/site-policy/blob/main/CONTRIBUTING.md) in the `site-policy` repository.hub.com/RikkaApps/websites/pull/79#issue-1751837442)

:::

### Start with root

For rooted devices, just start directly.

### Start via wireless debugging

Starting with wireless debugging works on Android 11 or above. This startup method does not require a connection to a computer. Due to system limitations, the startup steps need to be performed again after each reboot.

#### Enable Wireless debugging

1. Search the web for how to enable "Developer options" for your device model
2. Enable "Developer options" and "USB Debugging"<br><br><img :src="$withBase('/images/enable_dev_options.png')" style="max-width:320px;width:100%">
3. Enter "Wireless debugging"<br><br><img :src="$withBase('/images/enter_wireless_debugging.png')" style="max-width:320px;width:100%">
4. Enable "Wireless debugging"<br><br><img :src="$withBase('/images/enable_wireless_debugging.png')" style="max-width:320px;width:100%">
   
#### Pairing (only needs once)

1. Start pairing in Shizuku<br><img :src="$withBase('/images/start_paring_from_shizuku.png')" style="max-width:320px;width:100%">
2. [Enable Wireless debugging](#enable-wireless-debugging)
3. Tap "Pair device with pairing code" in "Wireless debugging"<br><img :src="$withBase('/images/start_pairing.png')" style="max-width:320px;width:100%">
4. Enter pairing code in Shizuku's notificaiton<br><img :src="$withBase('/images/enter_pairing_code.png')" style="max-width:320px;width:100%">

#### Start Shizuku

<img :src="$withBase('/images/start_shizuku.png')" style="max-width:320px;width:100%">

If it does not start, try disabling and enabling wireless debugging.

### Start by connecting to a computer

This boot method works on unrooted devices running Android 10 and below. Unfortunately, this startup method requires a computer. Due to system limitations, the boot steps need to be performed again after each reboot.

#### What is `adb`?

Android Debug Bridge (`adb`) is a versatile command-line tool that lets you communicate with a device. The adb command facilitates a variety of device actions, such as installing and debugging apps, and it provides access to a Unix shell that you Can use to run a variety of commands on a device.

See [Android Developer](https://developer.android.com/studio/command-line/adb) for more information.

#### Install `adb`

1. Download "SDK Platform Tools" provided by Google and extract it to any folder

   * [Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
   * [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip)
   * [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip)

2. Open the folder, right click to select

   * Windows 10: Open PowerShell windows here (**hold down Shift to show this option**)
   * Windows 7: Open command window here (**hold down Shift to show this option**)
   * Mac or Linux: Open Terminal

3. Enter `adb`, if success, you can see a long list of content instead of the prompt not finding adb.

::: tip
1. Please do not close this window. The "terminal" mentioned later refers to this window (if you closed the window, please go back to step 2)
2. If you use PowerShell or Linux/Mac, all `adb` should be replaced with `./adb`
:::

#### Setting `adb`

To use `adb` you first need to turn on USB debugging on your device, usually by following these steps:

1. Open system Settings and go to About.
2. Click "Build number" quickly for several times, you can see a message similar to "You are a developer".
3. At this point, you should able to find "Developer Options" in Settings,  enable "USB Debugging".
4. Connect the device to the computer and type `adb devices` in the terminal.
5. At this time, the dialog "Allow debugging" will appear on the device, check "Always allow" and confirm.
6. Enter `adb devices` again in the terminal. If there is no problem, you will see something like the following.

   ```
   List of devices attached
   XXX      device
   ```

::: tip
The steps for enabling Developer Options on different devices may vary, please search for yourself.
:::

#### Start Shizuku

Copy the command and paste into the terminal. If there is no problem, you will see that Shizuku has started successfully in Shizuku app.


::: details Command for Shizuku v11.2.0+

```
adb shell sh /sdcard/Android/data/moe.shizuku.privileged.api/start.sh
```
:::

## FAQ

Many manufacturers have made modifications to the Android system that prevent Shizuku from working properly.

### Start via wireless debugging: keeps showing "Searching for pairing service"

Please allow Shizuku to run in the background.

Searching for pairing service requires access to the local network, and many manufacturers disable network access for apps as soon as they become invisible. You can search the web for how to allow apps to run in the background on your device.

### Start via wireless debugging: immediately fail after tapping "Enter pairing code"

#### MIUI (Xiaomi, POCO)

Switch notification style to "Android" from "Notification" - "Notification shade" in system settings.

### Start via wireless debugging/Start by connecting to a computer: the permission of adb is limited

#### MIUI (Xiaomi, POCO)

Enable "USB debugging (Security options)" in "Developer options". **Note that this is a separate option from "USB debugging".**

#### ColorOS (OPPO & OnePlus)

Disable "Permission monitoring" in "Developer options".

#### Flyme (Meizu)

Disable "Flyme payment protection" in "Developer options".

### Start via wireless debugging/Start by connecting to a computer: Shizuku randomly stops

#### All devices

- Make sure Shizuku can run in the background.
- Do not disable "USB debugging" and "Developer options".
- Change the USB usage mode to "Charge only" in the "Developer options".
  
  On Android 8, the option is "Select USB configuration" - "Charge only".
  
  On Android 9+, the option is "Default USB configuration" - "No data transfer".

- (Android 11+) Enable "Disable adb authorization timeout" option

#### EMUI (Huawei)

Enable "Allow ADB debugging options in 'Charge only' mode" in "Developer options".

#### MIUI (Xiaomi, POCO)

Do not use the scan feature in MIUI's "Security" app, since it will disable "Developer options".

#### Sony

Don't click the dialog shows after connecting the USB, because it will change USB usage mode.

### Start via root: cannot start on boot

Please allow Shizuku to run in the background.
