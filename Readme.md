#Butler XT2 Standalone Starter Show
This show file is intended to provide a template to start from as well as an out-of-the-box test show to send with samples and for preliminary testing by fixture before installers before a commissioning agent arrives on a job-site.

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



