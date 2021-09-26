---
title: gShogi
layout: default
---

<table class="content">
    <tbody>
        <tr>
            <td class="navtop_left"></td>
            <td class="navtop_mid">
                <p style="float: left;">gShogi</p>
            </td>
            <td class="navtop_right"></td>
        </tr>
        <tr>
            <td class="navmid_left"></td>
            <td id="contentId" class="content_mid">      
                <p class="header">gShogi - An open source Shogi Game</p>        	    	    
	            <p class="centeredImage">
                    <a href="/images/Screenshot-gshogi-fullsize.png"> <img src="/images/Screenshot-gshogi-big.png" alt="gshogi screenshot" /></a>        
                </p>
                <p class="maintext"> 	    
	                gShogi is an open source Shogi (Japanese chess) game written in Python 3 and C for GTK 3 desktops. 
                    It has a built in engine (based on GNU Shogi) and you can also play against USI engines.
                    You can play handicap games and use western pieces (good for beginners) and study games saved
                    in the PSN format.            
                </p> 
 
                <h2>Features</h2>           
                <ul class="bullets">            
                    <li> Load / Save Games in native format or PSN format including support for reading multi-game files</li>           
                    <li> Set level of play (byoyomi, classical, incremental, fixed time per move, depth, infinite and nodes USI time controls)</li>
                    <li> Undo / Redo Moves</li> 
                    <li> Choose eastern or western pieces or load your own custom pieces</li>              
                    <li> Resizable Board</li>
                    <li> Builtin engine</li> 
                    <li> USI support - you can play against USI engines</li>
                    <li> Play human vs engine, engine vs engine or human vs human</li> 
                    <li> Play Handicap games</li>
                    <li> Customisable colours</li>
                    <li> Windows to display USI engine output, debugging info, move list, comments and game list</li>
                    <li> Edit board position</li>
                    <li> Copy/paste board position/game list to/from clipboard</li>        
                </ul>          
          
                <h2>Download</h2>
                <p class="maintext">
	                Download Git Master: <a href="https://github.com/johncheetham/gshogi/tarball/master">.tar.gz</a> &nbsp;&nbsp; 
                        <a href="https://github.com/johncheetham/gshogi/zipball/master">.zip</a><br /><br />
	                Download Last Release: <a href="https://github.com/johncheetham/gshogi/archive/v0.5.1.tar.gz">.tar.gz</a> &nbsp;&nbsp;
                        <a href="https://github.com/johncheetham/gshogi/archive/v0.5.1.zip">.zip</a><br /><br />
                    Download windows version <a href="https://drive.google.com/drive/folders/0B91ZDRXsSFY9a3Zrckc5WXRjcms?resourcekey=0-HyLnXZOo_P5FQW2NB8qqlg&usp=sharing">here</a> <br /><br />      
                    <a href='https://github.com/johncheetham/gshogi'>View project</a> on GitHub<br /><br />
                    <a href='https://pypi.org/project/gshogi/#files'>View files</a> on <a href='https://pypi.org'>The Python Package Index (PyPI)</a><br /><br />               
                </p>       

                <h2>Screenshots</h2>          
                <p class="leftImage">        
                    <a href="/images/Screenshot-gshogi-windows-fullsize.png"><img src="/images/Screenshot-gshogi-windows-small.png" alt="gshogi screenshot open windows" /></a> 
                    <a href="/images/Screenshot-gshogi-western-big.png"><img src="/images/Screenshot-gshogi-western-small.png" alt="gshogi screenshot with western pieces" /></a>
                    <a href="/images/Screenshot-gshogi-engines1.png"><img src="/images/Screenshot-gshogi-engines1-small.png" alt="gshogi engine list" /></a>              
                </p>
                <p class="maintext">  
                    Click on the images to view a larger version.
                </p>

                <h2>Using Custom Pieces</h2>        

                <p class="leftImage">
                    <a href="/images/Screenshot-gshogi-custom-big.png"><img src="/images/Screenshot-gshogi-custom-small.png" alt="gshogi screenshot with custom pieces" /></a> 
                </p>

                <p class="maintext">  
                    You can customise gShogi by changing the colour scheme and by creating your own piece images which you can load in via the GUI.
                    Above is an example of gShogi using custom piece images. Click on the image to view a larger version.<br /><br />
                    Download the above pieces here&nbsp;&nbsp;<a href="https://github.com/bewille/Gshogi-Pieces">gshogi custom pieces</a>.<br /><br />                      
                </p>

                <h2>Game Files</h2> 
                <p class="maintext">
                    You can load games in PSN format including support for multi-game files.<br />
                    The <a href="http://lysenka.net/shogi/20/">Shogiviewer</a> website contains a games collection that you can use with gShogi.<br /><br />    
                </p>
 
                <h2>Using USI engines</h2>
                <p class="maintext"> 
                    USI is the Universal Shogi Interface. You can install USI engines and use
                    them with gShogi.<br /><br />
                    <a href="usi.html">More information on using USI engines with gShogi</a>.
                </p>
        
                <h2>Utilities</h2>
                <p class="maintext">
                    Bernd Wille has created some utilities for gshogi including converting kif, psn and ascii files into formats that gshogi can read.
                    See <a href="https://github.com/bewille/gshogi-utilities">https://github.com/bewille/gshogi-utilities</a> for details.<br />
                </p>
        
                <h2><a id="gse" href="#gse">GSE</a></h2>        
                <p class="maintext"> 
                    gse is a USI version of the gShogi engine.<br />
                    It runs on Linux and windows. <br />
                    It must be used in conjunction with a USI GUI such as gShogi on Linux or shogidokoro on windows.<br /><br />                

                    Downloads (Last update: 3rd May 2012)<br /><br />        
	                &nbsp;&nbsp;&nbsp;&nbsp;<a href="gse-0.1.6.tar.gz">gse-0.1.6.tar.gz</a> &nbsp;&nbsp;Linux source tarball<br /><br />
                    &nbsp;&nbsp;&nbsp;&nbsp;<a href="gse-win-0.1.6.zip">gse-win-0.1.6.zip</a> &nbsp;&nbsp;source code and windows executable<br /><br />

                    &nbsp;&nbsp;&nbsp;&nbsp;<a href='https://github.com/johncheetham/gse'>View project</a> on GitHub<br /><br />
                </p>
                <p class="leftImage">        
                    <a href="/images/Screenshot-gse-big.png"><img src="/images/Screenshot-gse.png" alt="gse screenshot" /></a>         
                </p> 
                <p class="maintext"> 
                    Screenshot of the gse engine playing against the Laramie engine on shogidokoro. Click on the image to view it at full size.<br />
                    Shogidokoro is a windows USI GUI which you can download from <a href="http://www.geocities.jp/shogidokoro/download.html">http://www.geocities.jp/shogidokoro/download.html</a>.          
                </p>
                <br />         
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

