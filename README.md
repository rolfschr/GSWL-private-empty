# GSWL-private-empty

This repository contains an empty data data folder that could be used with GSWL-ecosystem.
The structure is exactly as [GSWL-private](https://github.com/rolfschr/GSWL-private) but without any data.
Use this repo to setup your own personal finances in Ledger.
Read "Getting Started With Ledger" before following the instructions below.

First steps to get started with your own setup:

```bash
$ mkdir -p ~/src && cd ~/src
$ git clone https://github.com/rolfschr/GSWL-ecosystem.git
$ git clone https://github.com/rolfschr/GSWL-private-empty.git
$ MYDIR=personalfinance # unexisting dirname
$ mv GSWL-private-empty $MYDIR
$ cd $MYDIR
$ mkdir CSV && mkdir tmp # for CSV conversions
$ rm ./README.md && rm ./LICENSE # optional ;)
$ rm -rf .git && git init # start your own Git repo
```
Then:

- Define your Ledger accounts in ``meta.txt``.
- Define your bank accounts in ``bankaccounts.yml`` & CSV conversion aliases in ``alias.local``.
- Define your opening balance (current financial state) in ``journal.txt``.
- Setup your own report commands in ``reports.txt``
- Define your Tmux (or whatever) session (see [example](https://github.com/rolfschr/GSWL-private/blob/master/.tmuxinator.GSWL-private.yml)).

Optionally:

- Setup some aliases in your ``.bashrc``. See [here](https://github.com/rolfschr/GSWL-private/blob/master/.bashrc) for some ideas.
- Encrypt your personal folder (actually _not_ optional!).
- Define conversion rates in ``prices.txt`` if you use multiple currencies.
