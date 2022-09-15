# remove-picture-metadata

Before uploading any images to the internet, it's a good idea to remove all the metadata.

This is the simplest way I've found on Linux:

Install perl-image-exiftool:

```
sudo pacman -S perl-image-exiftool
```

Clear out all the metadata:

```
exiftool -overwrite_original -all=  /path/to/file
```

To inspect the metadata, use `imagemagick`:

```
sudo pacman -S imagemagick
```

```
identify -verbose image.png
```
