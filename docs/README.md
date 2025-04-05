# Docs

Notes

1. These docs are intended to be friendly and understandable for beginners, so anyone can rapidly assume ownership of this code.
2. Don't confuse these docs with the **Content Collection** called docs.

Recommended reading order:

1. [Tech Stack](./tech-stack.md) - Explains the choice of technologies used for this application, their limitations, and all the setup needed to get the site deployed to the internet.
2. [Project Structure](./project-structure.md) - Provides an overview of the project directory.
3. [Customization](./customization.md) - Points out the areas of highest impact for customization, and examples of this template's range.

## Git Quick Reference

### Understanding

A git **repository** is a collection of files and folders that are tracked by the version control system called **git**. Each **branch** of a repo is a separate line of development, and each branch can have its own set of files and folders. When you **checkout** a branch, you're telling git to switch to that line of development, and the files and folders in the repo will change to match the state of that branch. When you make changes to these files, you can **commit** them to the repository, which saves a snapshot of the files at that moment in time. You can then **push** these changes to a remote repository, like GitHub, where they can be accessed by others. In the git world, a **remote** is a repository that is hosted on a server (as in, the one you see on Github), and **origin** is the default name for the remote repository that the local repository was cloned from.

#### Your branches

- `main` is the default branch, the trunk of the tree. This branch is connected to the astrogon template, and just because of the way we're structuring this repo, where it's holding both your base site and the Advynt site, leave this branch alone.
- `www/main` is the branch that holds the base site. Whatever code is applied to this branch will be automatically published to the live website. It is very possible that all your code works on your local machine, but breaks on the remote server, causing your site to go down. For that reason, you should not push to this branch directly.
- `www/dev` is the branch intended for development of the base site.
- `advynt/main` is the branch that holds the Advynt site. All the same rules apply here as for `www/main`.
- `advynt/dev` is the branch intended for development of the Advynt site.

### Setup

- Clone the repo: `git clone https://github.com/Soulleopard/pages.git`
- Checkout the Advynt development branch: `git checkout advynt/dev`

### The Main Loop

Once you've made all the changes you want...

- Stage your changed files for commit: `git add .`
- Commit them, with a descriptive message: `git commit -m "message here"`
- Push the changes up to GitHub: `git push origin advynt/dev`

### Other Useful Commands

If there's a change to any of your Node packages: `npm install`
If you mess things up real bad and just want to revert to the last commit: `git reset --hard`
When you want to pull changes down from GitHub: `git pull origin main`

## See Also

[Astro Documentation](https://docs.astro.build) - The official documentation for Astro. If there's an Astro topic you're confused about, you can probably find a consise and clear explanation here.
