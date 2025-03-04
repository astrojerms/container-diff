# How to Contribute

We'd love to accept your patches and contributions to this project. There are
just a few small guidelines you need to follow.

## Setup

If you haven't written Go code on your machine before, first follow the official
Golang instructions for setting up your environment: https://golang.org/doc/code.html

Once you have your environment set up, create a fork of the container-diff repository
with your personal GitHub account. Then, clone the fork into your `$GOPATH`:

```bash
git clone git@github.com:<your_account>/container-diff.git
$GOPATH/src/github.com/astrojerms/container-diff &&
cd $GOPATH/src/github.com/astrojerms/container-diff &&
git remote add upstream git@github.com:astrojerms/container-diff.git
```

The last command here sets the official repository as an upstream repository for
your fork, so you can keep your fork in sync with `main`:

```bash
(container-diff) git pull upstream main && git push origin main
```

## Building

From the project root, run `make clean && make`.

## Code reviews

All submissions, including submissions by project members, require review. We
use GitHub pull requests for this purpose. Consult
[GitHub Help](https://help.github.com/articles/about-pull-requests/) for more
information on using pull requests.

## Contributor License Agreement

Contributions to this project must be accompanied by a Contributor License
Agreement. You (or your employer) retain the copyright to your contribution,
this simply gives us permission to use and redistribute your contributions as
part of the project. Head over to <https://cla.developers.google.com/> to see
your current agreements on file or to sign a new one.

You generally only need to submit a CLA once, so if you've already submitted one
(even if it was for a different project), you probably don't need to do it
again.

## Tests

Before sending a PR, please make sure the included tests pass.
You can run these by running

```shell
make test integration
```

from the project root.

You can also configure the included git hook to run tests automatically on commit.
To do so, run:

```shell
ln -s $(pwd)/hack/hooks/* .git/hooks
```

from the project root.

## Dependencies

This project uses [dep](https://github.com/golang/dep) for managing dependencies and the `vendor` directory.
You should not need to know about this tool unless you are trying to add a new dependency or update an existing one.

See the [dep documentation](https://github.com/golang/dep#adding-a-dependency) for information on how to add a dependency.
