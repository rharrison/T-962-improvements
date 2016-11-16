# Compiling with LPCXpresso

__THIS HAS ONLY BEEN TESTED WITH LPCXpresso v8.2.2 [Build 650] [2016-09-09]__

You will need to import the project into your workspace and make a few changes to the build environment in LPCXpress. These are shown in the images below :-

On the __Quickstart Pannel__ which by default is in the lower left quadrent of the IDE select __Import project(s)__ and follow the instuctions...

![Quickstart Panel](/doc_img/import.png)

Next go into the properties for the project and make sure the __Tool Chain Editor__ is set as below ...

![Tool Chain Editor](/doc_img/toolchain.png)

Finally in __Properties__ choose __Settings__. Then select __Dialect__ and make sure the Dialect is set to GNU C99 ...

![SETTINGS DIALECT](/doc_img/dialect.png)


# Compiling without LPCXpresso

We need the `gcc-arm-none-eabi` compiler, for example in Ubuntu:

```
sudo add-apt-repository -y ppa:terry.guo/gcc-arm-embedded
sudo apt-get update
sudo apt-get install gcc-arm-none-eabi
```

And then run

```
make
```

## Flashing in Linux

The makefile has a target to download and build the [lpc21isp utility from sourceforge](http://sourceforge.net/projects/lpc21isp/). Just run

```
make flash
```
and it wil be downloaded and compiled for you.
