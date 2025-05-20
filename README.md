# Vibe Git commit messages

Inspired by [fteem's Git semantic commits repo](https://github.com/fteem/git-semantic-commits).

## What is this?
Easily commit your agent-produced vibe code before correcting everything and making it somewhat prod-ready.

## Installation:

1. Clone this repo, preferably in your `$HOME` directory. 
```
git clone https://github.com/zenibako/git-vibe-commits ~/.git-vibe-commits
```

> Tip: If you're using Cygwin, open it and type `echo $USERPROFILE`. This will show you the location of the `$HOME` directory.

2. Install it as a set of bash scripts or git aliases:
  * bash scripts 
  ```
  cd ~/.git-vibe-commits && ./install.sh --scripts
  ```
  * git aliases 
  ```
  cd ~/.git-vibe-commits && ./install.sh
  ```

> Tip: Installation script is idempotent and could be harmlessly executed multiple times. It adds bash scripts to the PATH in your `~/.bashrc` or `~/.zshrc` files or adds git aliases to the `~/.gitconfig` file respectively (without any duplication).

3. Vibe away!

## Usage

New command -> what it does:

* ```git vibe "commit message here"``` -> ```git commit -m 'vibe: commit message here'```

If you would like to add an optional scope, as described [here](https://conventionalcommits.org/), use the '-s' flag and quote the scope message:

* ```git vibe -s "scope here" "commit message here"``` -> ```git commit -m 'vibe(scope here): commit message here'```

If you would still like to use your text editor for your commit messages
you can omit the message, and do your commit message in your editor.

* ```git vibe``` -> ```git commit -m 'vibe: ' -e```

## Uninstallation

You can manually uninstall `git-vibe-commits` by:
* Removing the added aliases from `~/.gitconfig`.
* Removing the line added to the `$PATH` variable from `~/.bashrc`.

## How to contribute
Open a pull request/issue or fork this repo and submit your changes via a pull request.
