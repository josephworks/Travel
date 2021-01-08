Travel
==

Fork of [Paper](https://github.com/PaperMC/Paper) aimed at improving server performance at high playercounts.

## Contact
[Discord](https://discord.gg/uHRrAAHZs2)

## How To (Server Admins)
Travel uses the same paperclip jar system that Paper uses.

You can download the latest build of Travel by going [here](https://ci.codemc.io/job/TravelMC/job/Travel/).

You can also [build it yourself](https://github.com/Spottedleaf/Travel#building)

## How To (Plugin developers)
In order to use Travel as a dependency you must [build it yourself](https://github.com/Travel/Travel#building).
Each time you want to update your dependency you must re-build tuinity.

Travel-API maven dependency:
```xml
<dependency>
    <groupId>com.travel</groupId>
    <artifactId>travel-api</artifactId>
    <version>1.16.4-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
 </dependency>
 ```

Travel-Server maven dependency:
```xml
<dependency>
    <groupId>com.travel</groupId>
    <artifactId>travel</artifactId>
    <version>1.16.4-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

There is no repository required since the artifacts should be locally installed
via building travel.

## Building

Requirements:
- You need `git` installed, with a configured user name and email. 
   On windows you need to run from git bash.
- You need `maven` installed
- You need `jdk` 8+ installed to compile (and `jre` 8+ to run)
- Anything else that `paper` requires to build

If all you want is a paperclip server jar, just run `./travel jar`

Otherwise, to setup the `Travel-API` and `Travel-Server` repo, just run the following command
in your project root `./travel patch` additionally, after you run `./travel patch` you can run `./travel build` to build the 
respective api and server jars.

`./travel patch` should initialize the repo such that you can now start modifying and creating
patches. The folder `Travel-API` is the api repo and the `Travel-Server` folder
is the server repo and will contain the source files you will modify.

#### Creating a patch
Patches are effectively just commits in either `Travel-API` or `Travel-Server`.
To create one, just add a commit to either repo and run `./travel rb`, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.

## License
The PATCHES-LICENSE file describes the license for api & server patches,
found in `./patches` and its subdirectories except when noted otherwise.

Everything else is licensed under the MIT license, except when note otherwise.
See https://github.com/starlis/empirecraft and https://github.com/electronicboy/byof
for the license of material used/modified by this project.

## Note

The fork is based off of aikar's EMC framework found [here](https://github.com/starlis/empirecraft)
