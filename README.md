# Brown University Northern Change Lab Repo

A centralized repository that links to the individual repos used by members of the [Northern Change Research Lab](https://northernchange.brown.edu/) at Brown. See [Resources.md](Resources.md) for an evolving list of useful tutorials and resources for programming in our research areas. Add whatever code you think is useful for remote sensing data analysis and miscellaneous coding. This [repo](https://github.com/ekcomputer/Northern_Change_Lab) is now maintained by Ethan Kyzivat.

## Description of repositories
- [Image-Proc](https://github.com/ekcomputer/Image-Proc)  A growing set of image processing functions in matlab
- [Riv2xls](https://github.com/ekcomputer/AcousticDoppler)  ADCP quality control galore!
- [geographic-functions](https://github.com/ekcomputer/geographic-functions)    A set of bash shell scripts using gdal for raster manipulation.
- [gps_scrripts](https://github.com/ekcomputer/gps_scripts) A collection of simple bash shell scripts for manipulating GPS files using teqc/bash.
- [water-mask](https://github.com/ekcomputer/water-mask)    Ethan's masters thesis paper!
- [kats_funcs](https://github.com/elezine/funcs) Katia's frequently used functions
- [random-wetlands](https://github.com/ekcomputer/random-wetlands) Ethan's main scripts for running UAVSAR classification and analysis with methane data
- [PixelClassifier-fork](https://github.com/ekcomputer/PixelClassifier-fork) Random forests classification for random-wetlands; heavily modified from [HMS-IDAC](https://github.com/HMS-IDAC/PixelClassifier)
- [pixel-smasher](https://github.com/ekcomputer/pixel-smasher) Satellite super resolution workflow, modified from [Xintao Wang](https://github.com/xinntao/BasicSR)

## Using git submodule

We are experimenting with git submodules to link working repos with this one so that changes can be synchronized without having to create copies of working scripts here. A better solution might be github project boards.

### To add a sub-repository:
``` 
$ git submodule add https://github.com/example/url.git
```
Then push as normal.

### To clone from a repository with sub-repositories:

Either use
``` 
$ git clone https://github.com/example/url.git
& git submodule update --init
```
or
```
$ git clone --recurse-submodules https://github.com/example/url.git
```

If you clone as normally, the subrepos will show up as empty directories, so if you want to actually have the scripts, you will need to follow the commands above.

### To fetch updates from the sub-repositories:
```
git submodule update --remote [SUBMODULE NAME]
```

Minute details on git submodule available [here](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

### Note on file sizes
The repo "pixel-smasher" contains model parameter files that take up a lot of space. If you don't need to actually run the GAN model, you may consider deleting model files (end in .pth).
