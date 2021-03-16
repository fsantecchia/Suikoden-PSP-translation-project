# Genso Suikoden: Tsumugareshi Hyakunen no Toki - English translation project
We need translators!

Do you want to help!?

https://github.com/fsantecchia/Suikoden-PSP-translation-project/discussions/2

# Demo

https://drive.google.com/file/d/1HnO-3adXZkmbHJfhu2oS0dOcIdboN3_x/view?usp=sharing

# Progress
Text blocks: 8 / 17002

Cinematics: 0 / 17

**15 March 2021**

Everything is in place to start working on this translation! Original texts, cinematics and all the utils that we need to rebuild and test the game. Would you like to help? We need translators! The idea is to start contributing to this repo so we can translate this game once for all.

**09 March 2021**

The idea of this project is to start translating the game from japanse to english and then from english to spanish. We have all the tools and processes ready for this.
I dont know japanase lol so I am going to watch some of the english walkthroughs on youtube for the game and "translate" at least the first 30 minutes to show you!

# Current Team
**Chopp2** -> Team Leader https://www.romhacking.net/community/2934/

# Credits

## **Gil_Unx**

Creator of the first english patch using google translator and developer of the main tools that the team uses. Also he managed to get the cinematics from the .dat file.

This project wouldn't exist without his contributions.

You can see his video on
https://www.youtube.com/watch?v=uPAV7TDUEnM&ab_channel=GilUnx


## **1vierock** 

Texture translations and improvements
https://gbatemp.net/threads/suikoden-hd-texture-translation.582196/

Intructions for 1vierock's patch:
1. Install PPSSPP.
2. Load up your rom.
3. Go to Game Settings > Tools > Developer Tools.
4. Check "Replace textures".
5. Inside your PPSSPP folder, there will be a folder somewhere called PSP (mine is in PPSSPP/memstick/PSP).
6. You should see a folder called TEXTURES. If not, make it and go in.
7. Create a folder called NPJH50535 (that's the ID of the game).
8. Copy the contents of the download above into that folder.
9. Check PSP/TEXTURES/NPJH50535/textures.ini exists.

# Development process
You need:
1. An .ISO from the game (you can create it using your original phisical disk).
2. Our python script developed by Gil_Unx.
3. EBOOT.bin updated by Gil_Unx to change the limit of chars per line from 20 to 50 and the amount of lines from 3 to 4.
4. Python 3.9.
5. UMDGen 4.0.

Steps:

1. Create a folder.
2. Add the python script and the .ISO in the folder.
3. Mount the .ISO and copy PSP_GAME/USRDIR/data.dat from the .ISO, add it inside the folder and unmount the .ISO.
4. Run `python suikoden-script.py` inside the folder and write `-x` when it asks for a param.
5. Update .TXT files and videos.
6. Run `python suikoden-script.py` inside the folder and write `i` when it asks for a param.
7. Replace original EBOOT.bin for our custom EBOOT.bin inside the .ISO using UMDgen, you can take a look at `UMDgen guide.pdf` to do this.
8. Enjoy!

Video editing:

https://psp.scenebeta.com/tutorial/crear-tus-gameboots-personalizados
http://pspfreakyd.blogspot.com/2008/02/tutorial-to-make-c-intro-gameboot-with.html
1. Grab any video from the dumps folder.
2. Update the video (we need it to be a .avi file)
3. Open Umd Stream Composer (if you use Windows 10, you have to rename the .exe to make it work http://endlessparadigm.com/forum/showthread.php?tid=2402) and build the new video file follow these steps
    1. Open UMD Stream Composer
    2. Click New > Clip name: test (or anyname you like) & Project name: work (or anyname you like) and click next
    3. Check Box: Tick PSP Movie Format (for game) and click Finish
    4. Click Video Source > Open > Open "test2.avi" (in desktop). Click OK
    5. Click Audio Source > Open > Open "test.wav" (in desktop). Click OK
    6. Click Run(R) > "Encode + Multiplex" and wait for the process to finish
    7. Click Close and exit the program (Need not save the project)
4. Replace file extension for .bin and override the file the in the TMP_DATA folder created by the python script.



