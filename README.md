# SafariBooks Downloader & ePub Generator + Using SSO (Unattended version)
SafariBooks-Downloader is a project created and maintained by [Nico Haenggi](http://www.nicohaenggi.com/).
This version is an unattended version to download books using SSO modified by [Adán Carrasco](http://adancarrasco.com/).

# Installation Guide

## How To Install

Install Node.js. We recommend the **LTS release**. The SafariBooks-Downloader has been tested on most node versions between **v4.4.5 and v.6.9.5** and should therefore cause no problems running on one of these versions. For more information about how to install it on your environment, see [Installing Node.js via package manager](https://nodejs.org/en/download/package-manager/). To verify your installation, run:

```bash
node -v
```

If a version is returned, you did successfully install Node.js. Next up, make sure npm is properly installed. To verify, run:

```bash
npm -v
```

If the command returns a version number, you're all set. Next, we'll clone the repository.

```bash
git clone https://github.com/adancarrasco/SafariBooks-Downloader.git
cd SafariBooks-Downloader
```

Install all the dependencies with npm.

```bash
npm install
```
Congratulations! You've successfully installed SafariBooks-Downloader.

## How To Run

You need to update the `cookie` property in the `.config` file + the `bookid` that you'd want to download.

#### From where can I get the cookie?
1. Open Safari Books Online and login in Chrome
2. Open the `Developer Tools`
3. Go to `Network` pane
4. Go to the book that you'd want to download (look for the book id in the url, for example: `9781491925607`)
5. Look and copy the `cookie` as in the following image
    ![chrome-console-screenshot]
6. Paste the `cookie` and `bookid` in `.config` file
7. Run the following command: `npm run safaribooks-downloader`

That's it, the epub will be created under `books` folder, if there's an issue you might need to create the folder by your own.


# Features
- [x] generating ePub with cover image, authors and publisher
- [x] custom stylesheets will be imported (only one currently)

# Credits
- [Nico Haenggi](http://www.nicohaenggi.com): conception & development
- [cyrilis](https://github.com/cyrilis): a big thanks to cyrillis for his epub-gen package which I relied upon heavily while integrating my own epub generator
- [Adán Carrasco](http://adancarrasco.com): Unattended version for SSO usage via cookie

# Copyright & License

Copyright (c) 2017 Nico Haenggi - Released under the [MIT License](https://github.com/nicohaenggi/SafariBooks-Downloader/blob/master/LICENSE)

If you want to use this using normal login please follow the instructions in: [SafariBooks-Downloader](https://github.com/nicohaenggi/SafariBooks-Downloader)

[chrome-console-screenshot]: http://adancarrasco.com/sbd-chrome-console-screenshot.jpg