<a href="https://zerodha.tech"><img src="https://zerodha.tech/static/images/github-badge.svg" align="right" /></a>

# gtbump
git tag bump: A simple utility to bump and manage semver git tags and generate Markdown changelogs.

This is a fork of the original [repo](https://github.com/knadh/gtbump) removing the need of the `v` prefix before tags to better suit
the current standard at Delfos.

## Install
```shell
pip install gtbump
```

### Usage
```shell
# cd to your git repo.

# see the last tag.
$ gtbump --show
no tags found. Run --init to add 0.1.0

# add a tag for the first time.
$ gtbump --init
bumped 0.0.0 -> 0.1.0

# bump major | minor | patch
$ gtbump --minor
bumped 0.1.0 -> 0.2.0

$ gtbump --major
bumped 0.2.0 -> 1.2.0

# delete the last tag
$ gtbump --delete-last
deleted 1.2.0

# push the last tag upstream(or --push-last=your_remote_name)
$ gtbump --push-last
pushing 0.3.0 to origin

# generate changelog for the latest tag. This can be copy-pasted into GitHub's release description.
$ gtbump --changelog
changelog for 1.0.0 -> 1.1.0
- b361292 Display app version the settings UI
- a3b285f Fix Buefy number input width
- 63520d2 Merge pull request #388 from dunklesToast/chore/update-german-translations
- 3abac31 chore(translations): improve german translations
- 3ecac76 Fix Vue linting issue
```

Check `gtbump --help` for more options.

Licensed under the MIT license.
