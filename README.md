# DSFE labs

Repository for labs, for Data Science for Everyone course at UoB.

## Hub

Consider installing the [hub utility](https://hub.github.com).

## Workflow

### Initial clone

Clone the main repository: <https://github.com/matthew-brett/dsfe-labs>:

```
git clone https://github.com/matthew-brett/dsfe-labs
```

Check you now have your remote set up right:

```
cd dsfe-labe
git remote -v
```

You should see:

```
origin	git@github.com:matthew-brett/dsfe-labs.git (fetch)
origin	git@github.com:matthew-brett/dsfe-labs.git (push)
```

### Make a fork

If you have `hub` (above), run `hub fork` from the `dsfe-labs` directory.  Then you're done - you have a fork of the repo up on Github, and a local Git *remote* to match - check with `git remote -v`.

Otherwise go to the main repository page at
<https://github.com/matthew-brett/dsfe-labs>.  Click the "Fork" button near the
top right.  You will then get redirected to
`https://github.com/my-gh-user-name/dsfe-labs`, the URL for your fork of the
repo.  Copy the URL.  Go back to your terminal, and the `dsfe-labs` directory:

```
git remote add my-gh-user-name https://github.com/my-hg-user-name/dsfe-labs.git
```

Check you have a new remote:

```
git remote -v
```

Now you should get something like:

```
origin	git@github.com:matthew-brett/dsfe-labs.git (fetch)
origin	git@github.com:matthew-brett/dsfe-labs.git (push)
my-gh-user-name	git@github.com:my-gh-user-name/dsfe-labs.git (fetch)
my-gh-user-name	git@github.com:my-gh-user-name/dsfe-labs.git (push)
```

### Make a branch to work on

When you are ready to do some work, make a branch, with a name that matches the work you will do:

```
git branch suggest-labs-template
git checkout suggest-labs-template
```

Do some work, then `add` and `commit` it.

Then push up to Github with something like:

```
git push my-gh-user-name suggest-labs-template --set-upstream
```

As y'all remember, `--set-upstream` tells git that this branch has a permanent association with the "upstream" Github branch at `my-gh-user-name/suggest-labs-template`.

### Make a pull request

When you are ready, and you've pushed your work to Github, make a pull request.

If you're using `hub` - `hub pull-request`.  Enter message, and you're done.

Otherwise, go to the Github page for your fork, e.g.
`https://github.com/my-gh-user-name/dsfe-labs`, and you should see a button to
click, to make a pull request from this new branch, near the top of the page.
Use this, if you see it.  If you don't see it, go the URL
`https://github.com/my-gh-user-name/dsfe-labs/branches`, select the branch you
want to make a pull request from, and proceed from there.
