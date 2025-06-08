# ChessSpoon
Example UCI chess interface in C#.

June 8, 2025

This is a simple C# project to show chess UCI communications with an engine.  The code was developed using examples under the GPL, and you can use this code as permitted under GPL.  There is little error-checking so this program will snap crackle and pop if the FENs are wrong, or you're engine path is wrong, or any number of other common and uncommon issues.  I have only run this program in the debug environment.

Paul Fargen 

Example of using:
1.  Start the program.  A form and a console will start. 
2.  Double-click the EnginePath\Name.EXE text box at the top, and browse to your engine.
3.  Click the Start UCI Engine button.  This will start the engine listed in the box and activate other buttons on this form.  You might see some text on the console screen from the engine.
4.  Click the Send UCI+isready button.  This sends the first two commands to get the UCI ready.  Alternatively, these commands are available one at a time from the list.
5.  Clicking the Send to UCI Engine button will send the command appearing in the command textbox.  By default, this is ucinewgame.  The first three commands seem to be fairly common when the engines are started.
6.  Now select a command from the list on the right by clicking it.  This command populates the command textbox.  You then click the "Send To UCI Engine" button to send it to the engine.
7.  Sending some of the commands that begin with "position" or "position fen" will send board state.  You can verify with the "d" command if you are using Stockfish, or other engine that supports the "d" command.
8.  To have your engine calculate for two seconds, click the "go movetime 2000" item in the list, and then the "Send To UCI Engine" button.  You should see the engine output.  It will finish with a "bestmove xxxx" response.
9.  Look at the code for ClassUCI for ReadEngineMessage.  Here will be the Engine Message string that you can parse as you require for your application.
10.  Press the Quit button to kill the engine.

I'm a newbie at MS c# 2022 Community and UCI programming, which is why I searched for something like this, and ended up building it from other examples.  Alternatively, You can also start Stockfish or whatever in a Command Window and type commands into the console to see how the engine responds.  

