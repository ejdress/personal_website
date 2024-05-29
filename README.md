The project folder can be locally found in `~/projects` in old Matilda.

In order to update the website, you need to update the content of the `content` folder on GitHub. They are Markdown files.

Once you have updated them on GitHub, the rest of the steps need to be done locally. Navigate to a folder where you have cloned the GitHub repo to (see above), and then `git pull` to make sure your local content is up to date with the GitHub content.

Then you need to push the content of the updated website to the `gh-pages` branch of this repository. The instruction to do so is in this website.
The instruction for deploying the website can be found at https://docs.getpelican.com/en/latest/tips.html#publishing-a-project-site-to-github-pages-from-a-branch

Essentially, you need to run the following three lines of commands.
```bash
$ pelican content -o output -s pelicanconf.py
$ ghp-import output -b gh-pages
$ git push origin gh-pages
```

To do so, open you Anaconda command prompt, `conda activate analysis`, and then run these commands. After the last line, you will be asked to provide your GitHub loging credentials.

Actually, you can also do this from new Matilda, which might be a nicer workflow since you have Ubuntu WSL installed into new Matilda.
