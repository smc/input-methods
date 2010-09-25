This is a description about Enhanced Remington Typewriter Keyboard Layout mapping for m17n used in Gnu/Linux systems to input Unicode Malayalam characters. The mapping file was authored by Sebin Abraham Jacob <sebinajacob@gmail.com> of Swathanthra Malayalam Computing <http://smc.org.in>, an advocacy group for localisation and promotion of free sofware. The icon file was created by Hiran Venugopal <hiran.v@gmail.com> of SMC. This file should be maintained in UTF-8 encoding. 

History of Remington Layout

Initially, there were two typewriters that were used to type Malayalam Language text, one among them being Remington. Typewriter Malayalam had much limitation as there were no way to include all of the complex characters in available keys.  So "koottaksharams" were typed using a virama (chandrakkala) in between. Later, when computers began to be deployed, Ascii fonts were hacked to display Malayalam glyphs. So the remington keyboard layout for inputting Malayalam was ported to the external input method used in computers. As there were many players working in these area, the computer adaptation of the keyboard varied much. Though the base keys were the same, Koottaksharams were mapped in different locations. The way short vowels were made long vowels were different in different adaptations. This keyboard layout that you use now has been mapped after studying most of the major adaptations and converging it with my own logic. 

Major changes and features

No more Link key (Nuk key). In supersoft's adaptation of remington layout, / was used as link key. They themself discontinued its use after they made a unicode enabled version of their layout and instead placed the letter "ഢ" there. Also, they introduced the use of സ്റ്റ in | position.

Ralminov who introduced his own version of remington layout to use in Windows XP OS took away സ്റ്റ from that position and placed ക്‍ (chillu of ക) there. He also placed a non joiner virama at were we see a + sign in English Keyboard. 

Both these layouts didn't provide a way to type Malayalam digits. So I have included Malayalam digits instead of its English counterpart in this adaptation. Those who want to type English digits should switch back to English Keyboard. 

I have also continued the use of ക്‍ in the same postion were Ralminov mapped it. 

The non joiner chandrakkala were taken off from the new layout and instead ൗ sign has been placed. This is an addition to the already existing ൌ sign, which some consider archaic.

Semicolun was available in the position of colun in CDAC's adaptation of the layout. Though it had been discontinued by Ralminov, I have bought it back in use. Instead ZWSP, a non assigned character in Malayalam was avoided. 

CDAC's adaptation of Remington keyboard had a special key assigned to convert  LaghuSwaras (short vowels) into GuruSwaras (long vowels). This was only intended for the use of Swarakhsaras (vowels) and were not being used in Vyanjanas (consonants). This concept was discontinued in the unicode versions of the layout. But as the typists found it difficult to change the way they type, I was forced to include a weird logic were short vowels combined with the Dheergham (ാ) sign will produce its long vowel. 

In addition to that, I have also introduced another combination were the short vowels combined with its sign (that we use between consonants) will produce its long vowels. All these has been added after maintaining a way to type the long vowels directly. 

Additionaly, some rare letters in Malayalam that are almost out of use has been mapped newly into this layout. The particulars are as follows: 

ല്‍, the chillu form of ല combined with ു sign (post based form of ഉ) will produce ഌ. If the combination symbol is ൂ (post based form of ഊ), the resultant character will be ൡ. The letter ഋ combined with post based symbol of ഉ (ു) will generate ൠ. Also, when Sanskrit text is being written in Malayalam, the symbol Praslesham will be of use. A ഫ combined with visargam (ഃ) will produce ഽ now. These are totally my own additions to the layout. 

As SMC is still advocating non-atomic chillu characters, I have only included it in this map. But if anybody wants to input new chillu, either drop a mail or manually edit the bin file.

Installation instructions

In short: 
   
Download ml-remington.mim 
Keep it in /usr/share/m17n
Add the layout to your Ibus preferences.
Use the keyboard.

In detail: 
For Arch Linux users

first install yaourt from AUR

   $ sudo pacman -S yaourt


Then install ibus and related packages using yaourt. Yaourt will take care of packaging the source files for you.

   $ yaourt -S ibus ibus-table ibus-table-extraphrase ibus-m17n ibus-qt ibus-table-others ibus-table-quick


(NB: Some of these packages may not be needed. )



Common Steps:

Download ml-remington.mim file.

Assuming that, you have downloaded the same to ~/Downloads folder, Go to Terminal and type as following. (The part after $ sign)

   your-username ~ $ cd Downloads
   your-username ~ $ sudo mv ml-remington.mim /usr/share/m17n/


It will ask for password. Give it.

Now, edit your .bashrc file to include the below written lines. (Not necessary in Ubuntu). Append it to the end of the file.

   your-username ~ $ nano .bashrc


(Remember, there is a dot before bashrc as the file is hidden. To copy and paste, just select the lines written below, go to the file, and click on the middle mouse button.)

     export GTK_IM_MODULE=ibus
     export XMODIFIERS=@im=ibus
     export QT_IM_MODULE=ibus


Use Ctrl+X to exit nano. It will ask whether to save. Give Y.

Now logout and re-login. If everything goes Okay, your keyboard is ready to use.

Now, access Ibus preferences from

   System >> Preferences >> Ibus Preferences (in Ubuntu.)


or

   K >>  Applications >> Settings >> Ibus Preferences (in Arch linux / KDE)


Select the tab, <Input Method>.

There is a drop down menu <Select an input method>

Click on it and find remington (m17n) under Malayalam. Click on Add button. As you have placed three lines in your .bashrc, the ibus would automatically be invoked at startup. So better add ispell (m17n) under English too and keep it as default. The first entry would be default. You could move it up and down using the arrow keys.

(If you are in KDE, remember to switch off xkb layout by going to

K >> System Settings >> Hardware >> Input Devices >> Layouts >> Layout Indicator

and uncheck both <Show layout indicator> and <Configure Layouts>.

Now you could use Cntrl + Space to turn Ibus off or on. Also, you could use Ctrl + Shift to switch between different keyboard layouts. You could use as many layouts as you please. 

Resources

Wiki page for this layout can be accessed from http://wiki.smc.org.in/Remington A diagram of the layout can also be found in the wiki. 

Commit tree can be accessed from http://git.savannah.gnu.org/cgit/smc/input-methods.git/tree/m17n/ml-remington

A seperate copyright notice have been maintained in the file copyright.txt