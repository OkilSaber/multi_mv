# multi_mv
Basic python script to move and/or rename multiple folders at once

## Usage
```
$ ./multi_mv [mode] [path] [original] [new] [nb_times]
```
- `mode`: 1 or 2
  - 1: rename all folders which name contains `original` by replacing `original` by `new`
  - 2: Same as mode 1 but `original` must contain the flag `%nb`, this flag will be replaced by a number and will repeat the process going from 0 to `nb_times`
- `path`: path to the folder containing all the folders to be renamed, it must start from the root of the disk.
- `original`: string in the folders' name to be replaced
- `new`: string to replace `original`
- `nb_times`: see mode 2

## Example:
```
$ ./multi_mv 2 "~/Mangas/Tokyo Ghoul:re" "Vol.%nb " "" 16
```
This will replace 'Vol. 0 ' from 0 to 16 by nothing int the folders' names.

```
$ ./multi_mv 1 "~/Folders/" "Sessions " "Folders"
```
This will replace 'Folders' by 'Sessions' in the folders names.
