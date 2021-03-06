---
title: gShogi - USI Engines
layout: default
---

<table class="content">
    <tbody>
        <tr>
            <td class="navtop_left"></td>
            <td class="navtop_mid">
                <p style="float: left;">USI</p>
            </td>
            <td class="navtop_right"></td>
        </tr>
        <tr>
            <td class="navmid_left"></td>
            <td id="contentId" class="content_mid">
                <p class="header">Using USI Engines with gShogi</p>        
                <br />Page Last Updated: 24th March 2011<br /><br />
                <p class="maintext">	    
                    This page is part of the <a href="index.html">gShogi project</a>.
                </p>               
                <p class="maintext">
                    To use a USI engine you need to download it, install it, check it and then add it to gShogi.<br />
                    Here are some examples.
                </p>

                <h2>Lesserkai - An Example of Adding a USI Engine to gShogi</h2> 
                <p class="maintext">   
                    Lesserkai is an engine that comes with Shogidokoro. Shogidokoro is an excellent Shogi program for windows.<br />
                    The engine comes as source code that builds OK on Linux.<br /><br />
                    To use the Lesserkai engine use these commands to download, extract and build it:
                    <br />
                </p>
<pre>
wget http://www.geocities.jp/shogidokoro/download/LesserkaiSrc.zip
unzip LesserkaiSrc.zip
cd LesserkaiSrc/Lesserkai
make
</pre>
                <p class="maintext"> 
                    Note that if you download the zip with a browser it may be corrupted. Use wget to download it and it should work OK.<br /><br />
                    Now test it works. <br /><br />
                    First start the engine:
                    <br />
                </p>
<pre>
./Lesserkai
</pre>
                <p class="maintext"> 
                    It will wait for input.<br/><br />
                    Enter the command 'usi' and the engine should respond:
                    <br />
                </p>
<pre>
usi
id name Lesserkai 1.3.3
id author Program Writer
option name BookFile type string default public.bin
option name UseBook type check default true
usiok
</pre>
                <p class="maintext"> 
                    The 'usiok' response means the engine is working and should be OK to use with gshogi.<br /><br />
                    Now quit the engine by entering 'quit'.<br /><br />
                    Next add the engine to gShogi:<br /><br />
                    &nbsp;&nbsp;&nbsp;&nbsp;Start gShogi. It's best to start it from a terminal so you can see the output.<br />
                    &nbsp;&nbsp;&nbsp;&nbsp;Select options, then engines.<br />
                    &nbsp;&nbsp;&nbsp;&nbsp;click on the 'Add' button.<br />
                    &nbsp;&nbsp;&nbsp;&nbsp;Navigate to the Lesserkai executable with the path  LesserkaiSrc/Lesserkai/Lesserkai<br />
                    &nbsp;&nbsp;&nbsp;&nbsp;click the open button<br/><br />
                    The Engine should now appear in your list of engines.<br /><br />
                </p>
                <p class="leftImage">
                    <img src="/images/Screenshot-gshogi-engines.png" alt="gshogi engines screenshot" />
                </p> 
                <p class="maintext"> 
                    Click OK<br /><br />
                    Now configure it:<br /><br />
                    &nbsp;&nbsp;&nbsp;&nbsp;Click on Options, then players in the menu bar.<br/>
                    &nbsp;&nbsp;&nbsp;&nbsp;Set the white player to Lesserkai 1.3.3 and click OK.<br/>
                    &nbsp;&nbsp;&nbsp;&nbsp;Click on Options, then configure engine 1.<br/>
                    &nbsp;&nbsp;&nbsp;&nbsp;You should see the options that you can set for Lesserkai<br />
                </p>
                <p class="leftImage">
                    <img src="/images/Screenshot-gshogi-USI-Options.png" alt="gshogi configure screenshot" />
                </p> 
                <p class="maintext"> 
                    Note that these options are specific to the Lesserkai engine and will be different for a different USI engine.<br /><br />
                    Set the options, click OK, then you can start playing the game against the engine.<br /><br />
                    To add other USI engines you can follow a similar procedure.
                </p>

                <h2>gse - gShogi USI Engine</h2>
                <p class="maintext">
                    <a href="index.html#gse">gse</a> is a USI version of the gShogi builtin engine.<br />
                    It is basically the engine from GNU shogi with a USI wrapper.<br /> 
                    It runs on Linux and windows.<br /><br />
                    Download it from <a href="index.html#gse">here</a>.<br /><br />
                    To build it:
                    <br />
                </p>
<pre>
cd gse/src
make
</pre>
                <p class="maintext"> 
                    Then add the engine into gShogi the same way as for Lesserkai (navigate to gse/src/gse.sh when adding the engine).
                </p>

                <h2>GPSshogi</h2>
                <p class="maintext">  
                    GPSshogi was written by students of the University of Tokyo and won the World Computer Shogi Championships in 2009.<br /><br />
                    Here are instructions to compile it on Fedora 12. These are based on <a href="http://www.geocities.jp/ep3797/tips.html">these instructions</a>.<br /><br />

                    First download osl from http://gps.tanaka.ecc.u-tokyo.ac.jp/cgi-bin/viewvc.cgi/trunk/osl/.<br />
                    click on download gnu tarball and save the file. <br />
                    The file is called osl.tar.gz (3.1MB).<br /><br />

                    Next download GPSshogi from http://gps.tanaka.ecc.u-tokyo.ac.jp/cgi-bin/viewvc.cgi/trunk/gpsshogi/?root=gpsshogi.<br />
                    click on download gnu tarball and save the file. <br />
                    The file is called gpsshogi.tar.gz (23.3MB).<br /><br />

                    Now build it:
                    <br />
                </p>
<pre>
yum install boost boost-devel

tar xfvz osl.tar.gz
tar xfvz gpsshogi.tar.gz
    
cd osl/lib/third_party/tcmalloc-0.93
make
cd -
cd osl/release
make

cd -
cd gpsshogi/release
export BOOST_POSTFIX_MT=-mt 
make

cd -
mv gpsshogi/data osl/
</pre>
                <p class="maintext"> 
                    When adding it into gShogi you need to navigate to gpsshogi/release/gpsusi.
                </p>

                <h2>TJShogi - An Example of Adding a Windows USI Engine to gShogi Using Wine</h2> 
                <p class="maintext">  
                    Most USI engines are for Windows. Some of them will run in gShogi using Wine.<br />
                    Here I will use TJShogi as an example.<br /><br />
                    First install Wine:
                    <br />
                </p>
<pre>
yum install wine
</pre>
                <p class="maintext"> 
                    Next download the TJShogi engine:
                    <br />
                </p>
<pre>
wget http://tonyjh.com/chess/TJshogi.zip
unzip TJshogi.zip
</pre>
                <p class="maintext">
                    After extracting you should have a file called TJshogi.exe.<br />
                    Now set up a shell script called tjshogi.sh to run the program using Wine.<br />
                    It should be placed in the same directory as the TJshogi.exe program and should contain these lines:
                    <br />
                </p>
<pre>
#!/bin/sh

# tjshogi.sh - run TJshogi under wine

# change the working directory to the one the program is in
BASEDIR=`dirname $0`
cd $BASEDIR

# run the program with wine
/usr/bin/wine TJshogi.exe
</pre>
                <p class="maintext"> 
                    Note that the command to get the script directory uses backticks (not quotes).<br />
                    Now make it executable:
                    <br />
                </p>
<pre>
chmod a+x tjshogi.sh
</pre>
                <p class="maintext"> 
                    Test it works by running the shell script.<br />
                    Type in the 'usi' command. <br />
                    You should see:
                    <br />
                </p>
<pre>
usi
id name TJshogi 0.03
id author Tony Hecker
option name USI_Hash type spin default 32 min 4 max 512
option name USI_Ponder type check default true
usiok
</pre>
                <p class="maintext"> 
                    Enter 'quit' to quit the program.<br /><br />
                    Now add the engine into gShogi the same way as for Lesserkai except that when you add the engine
                    you need to navigate to the tjshogi.sh shell script.
                </p>

                <h2>Other Engines</h2>
                <p class="maintext"> 
                    Other Windows USI engines that you can use using Wine are Laramie, Blunder and Bonanza.<br /><br />
                    To use Blunder and Bonanza under wine you will need to install the windows version of mono.<br /><br />
                    To do this download mono from http://www.go-mono.com/mono-downloads/download.html.<br /><br />
                    Then install it using wine:
                    <br />
                </p>
<pre>
wine mono-2.6.7-gtksharp-2.12.10-win32-2.exe
</pre>
                <p class="maintext">
                    NB. You should install version 2.6.7 long term supported version and not the latest stable version 2.10.1.<br />
                    This works with both Blunder and Bonanza whereas 2.10.1 does not work with Bonanza (when tested on Fedora 14 64 bit).<br /><br />
                </p>

                <h3>Laramie</h3>
                <p class="maintext"> 
                    Download the file LaramieV3.zip from http://www4.ocn.ne.jp/~grf/shogi-laramie.html<br />
                </p>

                <h3>Blunder</h3>
                <p class="maintext"> 
                    Download the file Blunder-20090509-Binary.zip from http://hp.vector.co.jp/authors/VA039571/blunder/<br />
                    Note that later versions don't work with Wine.
                </p>

                <h3>Bonanza</h3>
                <p class="maintext"> 
                    Bonanza is not a USI engine but can be converted to USI using the U2B program.<br />
                    Download the file bonanza_v4.1.3.zip from http://www.geocities.jp/bonanza_shogi/<br />
                    Then download the file u2b.zip from http://www.geocities.jp/shogi_depot/<br />
                    you need to copy u2b.exe into the same folder as bonanza.exe and point your Wine shell script at u2b.exe.
                    <br />
                </p>
            </td>
            <td class="navmid_right"></td>
        </tr>
        <tr>
            <td class="navbot_left"></td>
            <td class="navbot_mid"></td>
            <td class="navbot_right"></td>
        </tr>
    </tbody>
</table>

