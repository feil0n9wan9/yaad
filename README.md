	,--.   ,--.,---.    ,---.  ,------.   
	 \  `.'  //  O  \  /  O  \ |  .-.  \  
	  '.    /|  .-.  ||  .-.  ||  |  \  : 
	    |  | |  | |  ||  | |  ||  '--'  / 
	    `--' `--' `--'`--' `--'`-------'  
# Yet Another Andorid Decompiler
#### Migrated from [RichieWan9/decompile](https://github.com/RichieWan9/decompile)


## Introduction
YAAD is yet another andorid decompiler for reverse engineering android apk, framework jar or optimized apk(odex) from ROM built with user tag. When developing on platform sdk, android build tools export a apk which contains all things(resources, dex(code), certificate, etc), but in case developing on Android Open Source Project(known as AOSP), it divides into three cases: normal apk, framework jar containing only code and optimized apk(odex) which separates code into a odex file from resources in apk. YAAD can detect and handle all these cases automatically.


## Usage
```bash
USAGE: yaad [options] <apk|jar|odex>

OPTIONS:
-s, --system=<directory>        The directory to look for framework odex files when decomile a odex file.
                                Defaults to the $YAADROOT/system directory.
	
-h, --help                      Print this help and exit.
```

To decompile a odex file, it also needs a few of framework odex files. What framework odex files needed depend on the optimized apk you are decompiling. The most used framework odex files are android.policy.odex, bouncycastle.odex, core.odex, pm.odex, core-junit.odex, ext.odex, services.odex, which you can pull from /system/framework directory in the device at which your optimized apk is compiled aimed. YAAD will give you tips when needed framework odexs not fond.  


## TODO
Things that i'd like to do:
* ✓ decomile android apk, framework jar and optimized apk(odex)
* implemeted as POSIX compatible function
* should work on sh, dash, bash, ksh, zsh
* dependencies can upgrade independently
* improve error handling
* make it rock!


## License
Copyright (c) 2016 Feilong Wang. Licensed under the [Apache License Verson 2.0](https://github.com/feil0n9wan9/yaad/blob/master/LICENSE)
