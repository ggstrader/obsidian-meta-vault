# obsidian-meta-vault
A repository for custom Obsidian.md dashboards, daily notes, etc.

Clone using:
```sh
git clone https://github.com/ggstrader/obsidian-meta-vault.git --recurse-submodules
```

# I'm not very technical, how do I use this thing?
The simplest way to get started is to go to [releases](https://github.com/ggstrader/obsidian-meta-vault/releases/) and download `obsidian-meta-vault.zip` from the latest release. When you unzip it, you'll see folders like "Dailies." Each folder inside will have a number like '0001.' You can open each of these as it's own vault. You may need to enable community plugins when you do so.

# I am somewhat technical, how do I use this thing?

The repo utilizes submodules to make it easier for devs to work on and update their snippets, dashboards, etc. without having to get approval for every change, and to still own their own work. It also makes it easier to "freeze" the submodules in time for specific versions of obsidian.

In order to add to this repository you must first:
- In your repository:
  - Name your repository `daily-note-n`, `dashboard-n`, etc. where n is the next available four digit number
  - ensure all of your changes are pushed, and run `git tag -a v1.0.0 -m "initial"; git push --tags`
- In this repository:
  - Fork this repo
  - clone (without --recurse-submodules)
  - add your repository as a submodule like so:
    - `git submodule add YOUR_REPO_URL ./Dailies/n; cd ./Dailies/n; checkout v1.0.0;` where n is again your four digit number and "Dailies" is the appropriate directory
    - run `cd ../..; git add .; git commit -m "added submodule"; git push`
  - submit a pull request on your fork

