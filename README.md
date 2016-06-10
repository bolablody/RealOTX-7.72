Features
=
    - Engine: OTX 2.X.S.4 LORD ZEDD: https://github.com/mattyx14/otxserver/tree/otxserv2/path_7_x
    - Real Map 7.72
    - Real Npcs 7.72
    - Real Monsters
    - Real Spells
    - CastSystem (Reqired create account with number "10")
    - AntiDupe Items
    - WarSystem (Withouth Shields)
    - AutoStack
    - Offiline Training
    - Stamina (Work with !stamina)
    - Stacked Parcels/Boxes/Crates etc is blocking movement
    - Loot message on screen
    - Party Shared Exp
    - Spells unlocked by reaching required magic level for specific spell
    - Bank system
    - All functions introduced since 7.4 at 9.85 - And many more....

Compatible AAC:
=

    [Gesior2012](https://github.com/gesior/Gesior2012/tree/TFS-0.4_rev_3703%2B).

    [ZnoteAAC](https://github.com/Znote/ZnoteAAC).

    [BitAAC](https://github.com/bitaac/bitaac).


How To Compile
=
A. Windows:

COMPILING IN WINDOWS OTX SERVER 2.X.S.4

   1. Download the required software
   To compile The OTX Server on Windows, you will need:
     
Visual Studio 2015 Enterprise: [VS2015](https://go.microsoft.com/fwlink/?LinkId=691979&clcid=0x409/)

Libs (libraries) 2.1: [Libs 2.1](https://mega.nz/#!ocIyHZxI!jMVyKCpsofbuuNbdsLhblHhJRbsZrz4u5_JHPGXKJuE/)

Boost C++ libraries

   32-bit download: [32-bit](http://sourceforge.net/projects/boost/files/boost-binaries/1.60.0/boost_1_60_0-msvc-14.0-32.exe/download/)
   
   64-bit download: [32-bit](http://sourceforge.net/projects/boost/files/boost-binaries/1.60.0/boost_1_60_0-msvc-14.0-64.exe/download/)

   2. Install the required software
Once you have downloaded the software listed in the step above, begin by installing Visual Studio and Boost C++ libraries. Extract "tfs-sdk-2.1" anywhere on your computer and run the file "registerenv.bat" to set the PATH environment variable for "SQK-NOBOOST", so that the compiler can find the libraries once we get to compiling the source code. Move the file "register_boost_env.bat" from "SQK-NOBOOST" to the directory where you installed Boost C++ libraries and run it there (it should be in the directory called for example: C:\local\boost_1_60_0).

   3. Download the source code
  
   If you have a Git client installed, you can clone the latest copy with this command:

   CodeGit:
        
        $ git clone https://github.com/brewsterl/RealOTX7.72.git
        
   Source RealOTX 7.72 (OTX Server 2):
   
        https://github.com/brewsterl/RealOTX7.72/archive/master.zip

   4. Open up ..\sources\msvc\TheOTXServer.sln, change from "Debug" to "Release or Release GUI" and simply build the project.

B. Linux:
A detailed and always up-to-date tutorial may be found here:
	Download required packages
        Launch a terminal, and paste in the following commands:
        
            apt-get install update
            apt-get install git subversion autoconf build-essential pkg-config libboost-dev libgmp3-dev libxml2-dev liblua5.1-0-dev libmysqlclient-dev ccache libboost-filesystem-dev libboost-regex-dev libboost-system-dev libboost-thread-dev screen libssl-dev

Compiling
   Download sources - Launch a terminal, and paste in this command:
            
    git clone https://github.com/brewsterl/RealOTX7.72.git

   Launch a terminal, and type this:
Into Folder run:

    sh ./autogen.sh && ./configure --enable-server-diag --enable-mysql --enable-groundcache --enable-root-permission && make -j 2
