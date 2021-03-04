# USF Website Sources

This repository contains the source code for the USF website. The website is generated with [hugo](https:/gohugo.io).

## Editing the website

To be able to edit the website and deploy it you need to have two things installed:

 - hugo 0.76 or newer
 - NPM for installing the dependencies

### Clone the Repository

This repository uses recursive submodules. In order to clone it run:

```
git clone --recurse-submodules https://github.com/universalsafetyformat/usf_website.git
```

### Install dependencies

After cloning the sources code run:

```
npm install
```

to install the required CSS tools.

### Edit

Edit the sources with your favorite editor. You can run `hugo server` in the background to get a live preview of your changes in the browser.

### Commit and Deploy

Commit your changes once you are finished.

Do deploy the website run `./deploy.sh` in the root of the repository. This will rebuild the website with hugo and push the changes to the github pages repository.

The github pages repository is included as a submodule to seperate the source code and the generate HTML, therefor please commit once more after you have ran the deploy script.