# Git Function Extensions

## Usage

```sh
$ cd $HOME
$ get clone https://github.com/bigdata-memory/git-ext
$ export PATH=$PATH:$HOME/git-ext/fns
```

## Functions

### `git find-largeblobs [-h] [-r] [-q] [-t] [-c <count>] [-p <pattern>]`

* `-h` - Show usage
* `-r` - Show size in human readable format
* `-q` - Suppress messages
* `-t` - Show total size
* `-c <number>` - The number of large blobs to find (default:5)
* `-p <pattern>` - The regex used to filter large blobs

list specified number of large files.

Example:
```sh
git find-largeblobs -c 10 -t -r -p "tar\.gz$"
```

### `git prune-largeblobs [-h] [-c <count>] [-p <pattern>]`
#### Prerequisites:
       1. [git-filter-repo](https://github.com/newren/git-filter-repo). For Ubuntu, `sudo apt install git-filter-repo --edge`
       2. Fresh clone repository.

* `-h` - Show usage
* `-c <number>` - The number of large blobs to find (default:5)
* `-p <pattern>` - The regex used to filter large blobs

list specified number of large files.

Example:
```sh
git prune-largeblobs -c 10 -p "tar\.gz$"
```
