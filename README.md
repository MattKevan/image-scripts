# Cloudinary framed image generator

Simple shell script to generate Etsy-ready framed and cropped product images from Cloudinary. The script will iterate through a batch of named and sequentially numbered images, generating a framed, full size and cropped version of each. 

Files will be output as Jpegs, no matter the source format.

1. Upload product images to Cloudinary
2. Run script
3. ...
4. Profit

## Usage

```
sh frame.sh [image shape] [start no] [stop no] [batch name] [output name]
```

For example:

```
sh frame.sh l 1 20 Buttterflies_8x10 Butterflies
```
### Image shape

The script can generate frames for square, A4 and 8x10 images, portrait or landscape.
* ```p``` = 8x10 portrait
* ```l``` = 8x10 landscape
* ```pa``` = A4 portrait
* ```la``` = A4 landscape
* ```s``` = square

### Start and stop numbers

Specify the number of images in a batch, e.g ```1 20``` if there are 20 images, or a custom sequential range within, e.g ```5 15```.

### Batch name

Make sure images uploaded to Cloudinary follow the pattern ```[batch name]_[number]```, e.g. ```Butterflies_1```. Use batch name without the underscorr and trailing number, e.g. ```Butterflies```.

### Output name

This is the saved filename for your images. This can be the same or different to the batch name. They will also be numbered sequentially.
