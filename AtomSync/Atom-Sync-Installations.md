# Syncing Atom settings & packages between installations

In order to harness the true power of Atom and truly reap the benefits of actually using to it's true potential, for most of us that work on more then one machine, it's actually pretty important to have it configured and setup only once and have it synced across all devices.

The easiest way (and I would say best from my point of view) is by using the [`sync-settings`](https://atom.io/packages/sync-settings) package, found in the official package manager.

As a prerequisite you need to have a valid GitHub account, but I don't image that's gonna be a problem.

1. In Atom, go to Preferences (`Cmd + ,` on a )

2. Tap on `+ Install`

3. Now search for `sync-settings` and tap Install

![](https://raw.githubusercontent.com/trusk89/Blog/AtomSync/AtomSync/1.png "")

4. Tap on `Settings` and this is where it gets interesting. `sync-settings` uses GitHub to actually sync a bunch of `.json` files that describe what you have installed and how Atom is configured.

5. The first thing we need to do, is to get you a [`GitHub personal access token`](https://github.com/settings/tokens/new)

  a. Use a suggestive token description. It doesn't really matter, you just want to know what it is 6 months down the line when you look at it and wonder if you should delete it.

  b. Now select the `gist` scope
  ![](https://raw.githubusercontent.com/trusk89/Blog/AtomSync/AtomSync/2.png "")

  c. Now tap on `Generate token` and this is **very important: copy the token and't don't love it. Save it somewhere private and safe! (you're gonna need it on all the devices you want to sync)**

6. Now let's create a new `gist`

  a. Go to https://gist.github.com/
  b. Set the name to `packages.json` (**very important**)
  c. Empty description or whatever
  d. Write some gibberish into the content. It's not important and it will be overwritten on the first backup.
  e. Tap on `Create secret gist` and you'll extract the gist id from the visible url (it's the last part, after the username)
  ![](https://raw.githubusercontent.com/trusk89/Blog/AtomSync/AtomSync/3.png "")

7. Now that we have both the secret token and the gist we're coming back into `Atom` and into `sync-settings` settings and fill them into to their respective fields
![](https://raw.githubusercontent.com/trusk89/Blog/AtomSync/AtomSync/4.png "")

And this is it on the configuration part. Now you can go on the toolbar to `Packages` > `Synchronize Settings` and tap `Backup` and you should see a green notification banner in the upper right corner telling you that the backup was successful.
