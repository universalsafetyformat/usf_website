# USF Website Sources

This repository contains the source code for the USF website. The website is generated with [hugo](https:/gohugo.io).

See [this page](https://github.com/universalsafetyformat/usf_website/wiki/Notes-on-licenses-of-used-frameworks-and-images) for details on licensing. 

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

Note: Running the deploy script didn't work with `node` version v9.5.0 (on MacOS BigSur). Switching to version v10.15.1 fixed the problem (e.g., using `nvm install v10.15.1`).

### Edit

Edit the sources with your favorite editor (see the folder `content/en`). You can run `hugo server` in the background to get a live preview of your changes in the browser (use URL "localhost:1313").

Look at the [Markdown Guide](https://www.markdownguide.org/tools/hugo/) to get more information about the markdown elements supported by [hugo](https:/gohugo.io) out of the box.

The website uses the Docsy template. Check out the [Docsy example site](https://www.docsy.dev/docs/), which serves as a blueprint what can be done with Docsy. The sources for the example site can be found [here](https://github.com/google/docsy/tree/a7dc77412c533fefc71730927350677fed35f576/userguide/content/en).

### Commit sources and review

Commit your changes once you are finished. Note that the github repository applies the following policy:

- the _master_ branch is protected and doesn't allow direct pushing
- create a branch and push your changes there
- create a pull request for the branch on github and trigger a review
- at least one approval is required in order to merge the pull request


### Deploy and publish

The github pages repository is included as a submodule to seperate the source code and the generate HTML, therefore please commit once more after you have ran the deploy script. Note that there is a similar policy on the github pages repository as described above:

- the _main_ branch is protected and doesn't allow direct pushing
- create a branch and push your changes there
- create a pull request for the branch on github and trigger a review (choose the same reviewer as for the source changes)
- at least one approval is required in order to merge the pull request

In order to deploy the website run `./deploy.sh` in the root of the repository. This will rebuild the website with hugo and push the changes to the github pages repository.

