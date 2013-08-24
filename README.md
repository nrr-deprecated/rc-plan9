# a curmudgeon's plan 9 scripts

this is part of a series.

## what is this?

these are my scripts and plumber rules for the various plan 9 tools.

## things to come

i want to keep fleshing this out as much as i can.

### get rid of the sourcery

i hope to make some of the actual development work for this suck less
since, well, it's kinda terrible at the moment. one thought is to do the
following:

    git clone --no-checkout github.com:nrr/rc-plan9.git
    git config core.worktree="../../"
    git checkout master

this has a number of benefits, namely

* changes to dotfiles are known to git without any sort of extra
  sourcery
* new files become known to git when they're created, again without any
  extra sourcery
* my home directory will itself not be a git repository, but it will
  nonetheless be versioned

### abuse git subtree

i do actually dislike the multi-repository madness that i have going on
between `rc`, `rc-bash`, and `rc-plan9`, but i also prefer it to having
everything under one giant repository.

at some point, i'd like to look at abusing `git subtree` to this end and
seeing what sort of extra sourcery it'll require to get to a workable
state.
