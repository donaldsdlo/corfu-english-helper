## What is corfu-english-helper ?
corfu-english-helper is english writing assistant, help me complete English word.

This plugin base on fantastic completion framework [Corfu](https://github.com/minad/corfu)

<img src="./screenshot.png" width="400">

## Install
This package is installed with `use-package` and `straight.el` (assume both are already configured in your init file):

```elisp
(use-package corfu-english-helper
  :straight (:host github :repo "manateelazycat/corfu-english-helper")
  :defer t)
```

Enable it with `M-x toggle-corfu-english-helper`, or bind it to a key of your choice, e.g.:

```elisp
(global-set-key (kbd "M-s M-s") #'toggle-corfu-english-helper)
```

## Usage
* ```toggle-corfu-english-helper```: toggle on english helper, write english on the fly.
* ```corfu-english-helper-search```: popup english helper manually


## Customize your own dictionary.
Default english dictionary is generate from stardict KDict dictionary with below command

```Shell
python ./stardict.py stardict-kdic-ec-11w-2.4.2/kdic-ec-11w.ifo
```

You can replace with your favorite stardict dictionary's info filepath to generate your own corfu-english-helper-data.el .

# Acknowledgements
I create [company-english-helper](https://github.com/manateelazycat/company-english-helper), this package is port to corfu-mode, most code of corfu version is written by [theFool32](https://github.com/theFool32).

# Change Log
- 2026-10-09: Convert to latest convention. Modernize the package header with `lexical-binding` and standard package metadata (Author/Maintainer/Copyright/Version/Package-Requires/URL); switch the install instructions in the README to `use-package` + `straight.el`; generated data file now carries a modern header.
