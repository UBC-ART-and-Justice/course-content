# course-content
This repository contains the course content that will be visible on the website, and will make up the contents of the android app.

## Installing and setting up MkDocs-Material

For full documentation visit [mkdocs.org](https://www.mkdocs.org)

If you are comfortable with git and the command line, you can run the project locally. This will allow you to see changes in real time and test out new features before pushing them to the live site.

Alternatively, you can edit individual files directly on GitHub. However, this is not recommended for large changes, as it can be difficult to see how everything fits together.

### Running the project locally

1. Install MkDocs Material using pip: `pip install mkdocs-material`. If you don't have pip, [see this page for alternative installation methods](https://squidfunk.github.io/mkdocs-material/getting-started/).
2. Install the following plugins that are being used for this project:

    -  `pip install mkdocs-glightbox`
    -  `pip install "mkdocs-material[imaging]`

3. From the root of the repository, run `mkdocs serve` and wait for the site to build. You should see a message that says `Serving on http://[...]`, which is the local address where you can view the site. You can copy and paste this address into your browser, or click on it if you are using a terminal that supports it.

### Useful commands

* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Live Hosting on GitHub Pages

This site is already set up to be hosted on GitHub Pages. In case there are issues, here are the steps to set it up:

1. In the repository root, create the file: `.github/workflows/ci.yml` with the content from [the project site](https://squidfunk.github.io/mkdocs-material/publishing-your-site/), as well as any additional plugins you are using.
2. Commit and push the changes to GitHub. This will trigger the GitHub Action to run through the steps in the file you just created (installing dependencies, building, and pushing the site to the `gh-pages` branch).
3. On GitHub, go to `Actions` and wait for the action to finish. You can check the logs to see if there are any errors.
4. On GitHub, go to `Settings` -> `GitHub Pages` and change the `Source` to  `Deploy from a branch` if it isn't already. You can then set the `Branch` to `gh-pages` and save. 
5. After everything is completed, you should see a link to your website either at the top of the `GitHub Pages` section or on the homepage of the repo under `Deployments`. 

The link should follow the format: `https://<username>.github.io/<repository-name>/`. If you don't see it, wait a few minutes and refresh the page.
