CIA building extension for pokecrystal
======================================

This repo provides a simple extension that integrates the build of a Virtual Console .cia file to pokecrystal, to ease the building of a VC .cia for your ROM Hack down to something as simple as `make cia`.

Requirements
------------

* A recent [pokecrystal](https://github.com/pret/pokecrystal) installation, that supports building Virtual Console patches.
* An original (encrypted or decrypted) Pokémon Crystal Version (English) .cia file.
* [ctrtool and makerom](https://github.com/profi200/Project_CTR) (Only master has been tested)

Obtaining the original file is outside of the scope of this document. It can be legally obtained by extracting it from your console through tools such as GodMode9 and/or FunkyCIA.

Run `make` to build both `ctrtool` and `makerom`, and put them in your `$PATH`.

Installation
------------

It shouldn't be more complicated than the following:
```
cd <path to pokecrystal>
git clone https://github.com/mid-kid/pokecrystal-cia vc
echo "-include vc/cia.mk" >> Makefile
```

Copy your original .cia file to `vc/0004000000172800.cia`.

Now you can run `make cia` and be on your merry way!
