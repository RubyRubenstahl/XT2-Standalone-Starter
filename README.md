#Butler XT2 Standalone Starter Show

This show file is intended to provide a template to start from, as well as an out-of-the-box test show to send with samples and for preliminary testing by fixture before installers before a commissioning agent arrives on a job-site.



>**Please note** this show file is optimized for working with RGB fixtures. The color picker and test cues may not work properly with other fixture types. All other features should work fine without any modifications.



###Features

 - 10 Universes of RGB fixtures patched and neatly arranged.

 - 10 Sample looks designed to provide attractive content for a generic set of RGB fixtures.

 - Action pad with buttons for all of the sample looks and a fully configured color picker.

 - Groups for all fixtures and each universe for easy testing.

 - Glass Touch T6R & T12 with buttons mapped to the sample scenes.

 - An editable PDF file for Glass Touch T6R and T12 for show documentation.

 - 6 Test Cues (Including RGB, CMYK, All On, and Random colors). 

 - Butler XT2 button A is set to cycle through the test cues.

 - Butler XT2 button B is set to turn the system off.

 - Mutex Groups are pre-configured.

 - Cuelist 1 is set to play on startup.

 - There are triggers pre-configured to bring the grandmaster up a half-hour before sunrise & down at 2am.

 - There are triggers in place to manage the handoff between standard looks and the color picker.

 - Cue defaults are set to work nicely for offline show use (0 second fade, 2 second wait) so that static cues will trigger the glass touch buttons/action pad indicators will stay lit when selected.

 - Utility scripts to assist in performing repetitive actions.

 ---

 



###Usage



####Glass Touch



To use the glass touch settings you'll want to open the device manager, run the Automatic Device Discovery Wizard (top-had button) to discover the new glass touch. Then you'll right-click on the template Glass Touch and select _Copy Control Settings_ then right click on the newly discovered Glass Touch and select _Paste Control Settings_. The settings should be then transferred over.



####Importing a new patch



When importing a new patch make sure that the _"Clear current Patch"_ checkbox is selected in the _Open_ dialog. This will clear out all of the existing fixtures before importing your new patch. 



>**Important!**

>When importing a new patch you will need to update the color picker cues in **QL13, QL14, and QL15** (red, green, and blue) in order for the color picker to work properly.



#### Adding new cues

When adding new cues to the show file, make sure to use _Mutex Group 1_ for any cues that will be added to the main zone. If you would like to add additional test cues that will be cycled with the A button on the Butler XT2, use _Mutex group 2_. 



#### Adding new ActionPad buttons

If you add a new Action Pad button for a _Mutex Group 1_ (main zone) cue, make sure that its release action is set to fire **Trigger Label 2**. This will ensure that the color picker and any test cues are stopped automatically when a standard cue is played.



If you are adding a new button for a test cue, you'll want to set the release action to **Trigger Label 3**



#### Test cues

For the test cues I've included both RGB and CMY versions. The RGB cues work well for testing LED fixtures when you can view them directly. When a fixture is behind diffusion, however, it can be difficult to see a node that is missing a color because the spot below just becomes a bit dimmer. Using CMY, however, it becomes much more obvious because, instead of just having a dim spot the color will display wrong. For example if you are using magenta (red + blue) and a blue LED is out there will be one spot that is just red, standing out well through diffusion. 



####  Utility Scripts

>**Important!**

>The included utility functions are dangerous and can overwrite and/or delete existing cues. These actoins can not be undone once performed. **Please read before using**.



There are several utility scripts included in the show file, all of which are accessible via the "Utilities" action pad page. 



##### ClearAllCuelists

This function will clear all cues in all cuelists without changing any other settings  (Name, mutex ID, etc) in those cuelists. This is helpful to clear out everything before you begin programming so that you don't have to delete the sample cue in each cuelist before recording your new cue. 



##### ClearSelectedCue

This will clear the currently selected cuelist, leaving all other settings (Name, mutex ID, etc) intact. 



##### DeleteAllGroups

Removes all existing groups from the show file. This is helpful when starting to program to remove all of the smaple groups without having to delete them each individually.



##### generateColorPickerCues

This will generate a red, green, and blue cuelist for use in the color picker. A dialog will be displayed asking for the first cuelist to use and the group that you'd like to use. By defaul the first group is used and the first cuelist (red) is set to 13 to match the layout of the *Starter Show* showfile.



##### generateTestCues

This will generate a series of 5 test cues. A dialog box will ask for the mutex group ID, fixture group, and first cuelist. It will then generate the following test cues:

	1. RGB Fade - Red, Green, and Blue cues with a 1 second fade and 2 second wait between each.

	2. RGB Snap - Red, Green, and Blue cues with a 0 second fade and a  1 second wait between each.

	3. CMY Fade - Cyan, Magenta, and Yellow cues with a 1 second fade and 2 second wait between each.

	4. CMY Snap -  Cyan, Magenta, and Yellow cues with a 0 second fade and a  1 second wait between each.

	5. All White - All fixtures 100% white. 



The cues are programmed to provide a seamless loop in offline mode.



By default the Mutex group ID is set to 2 and the first cuelist is 16 to match the layout of the *Starter Show* showfile.


##### setCuelistNamesByFirstCueName
This will present a dialog box asking for start and end cuelists. All cuelists in this range will have their name changed to match that of the first cue in each list. Any empty cuelits will be ignored. 


All of these utility scripts are accessible via buttons on the Utilities page of the Action Pad. You must first click the "I Understand" button under the warning before the buttons become visible.

##### setButtonNames
This script will copy the names of cuelists and apply them to their respective buttons in the Action Pad. 

To make this script work, each playback button in the Action Pad has a script ID set to `QLx`, where `x` is the number of the cuelist it represents. The script will loop through all numbers between 1 and 100; if a button exists for that cuelist, the name will be copied to it.

If you wish to add more buttons just copy an existing button, change the Action to play back the desired cuelist and then the script ID to match it. Next time you run the script, the new button will be included.




**It is highly reccommended** that you remove the utility page & scripts from the show file before turning it over to the end client.

 





