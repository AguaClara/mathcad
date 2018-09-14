# MathCAD Files

## What is this repo?

These are the old design tool files that were used to run the old MathCAD-based design engine.

They are ported over from a decommissioned svn repository into git.

We use git lfs to hold the large files. That speeds up the checkout process.

## Versions

SVN versions had associated numbers, starting from 0 and going up to 7825. These version numbers are how the old design tool tracked which iteration of the tool was creating the design. In MathCAD design tool lingo, we'd say something like "The Gracias plant was made with version 4931". Since converting to git, we can't directly search for the version. Instead, we have to use some program to hunt through the git commits and read all the git logs. This is much faster than I'm making it sound.

## Finding and checking out a version

1. Find the commit hash.
  * On both mac terminal and Windows **git bash**, you can use the following bash command: `git log --all --grep='design@4921'` to find the commit associated with version 4921.
2. Once you've found the relevant commit hash, you can "checkout" the version with `git checkout <commit hash here>`. For example, for the version 4921 that I found above, I would write `git checkout cbd1eee3eb3ea337458cf2a35bd877da92025ce4`.
3. You are now in `DETATCHED HEAD` state, meaning you can't change anything permanently. Instead, just look around for what you need, or run some MathCAD functions, etc...
4. To get back to the most recent version, run `git checkout master`.  
