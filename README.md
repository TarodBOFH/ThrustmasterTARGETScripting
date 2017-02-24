# ThrustmasterTARGETScripting

Sample script for Thrustmaster TARGET scripting in order to setup a single combined axis when using the toe brakes.

This script can be configured in a single file:

combined_pedals_settings.tmh

Settings:
 * Mode of combination
  - Merge: The axis value will be the difference between left toe and right toe
  - Greatest: The axis value will be the greatest value of both left and right toe
  Change the value of CombinePedalsMode to the one of your choice or uncomment / comment the premade definitions
  
 * Virtual Axis to use: Change the value of CombinePedalsAxis define to the one of your choice. By default it will use DX_SLIDER_AXIS
 
 * Disable toes: If you have mapped the toes to other axis (i.e. DX_XROT_AXIS or DX_YROT_AXIS) because you wanted to apply some curves, disable their default input with 1. This also will prevent to publish the Thrustmaster Rudder Pedals once launching the script. If you leave the default 0, your game will see both the virtual controller (and combined axis) as well as the physical controller. *DISCLAIMER* You cannot see the vcontroller on the 'Device Analyzer' while using the mode MODE_KEEPENABLED. Use ComboPedalsDebug on the 'combined_pedals_macros.ttm' file to debug with the device analyzer.
 * Setup curves for your brake toes with SetJCurve to apply it before calculations. It allows you have the brake toes with higher sensitive close to deadzone, for example.
  
## FIRST TIME SETUP
Enable ComboPedalsDebug to be able to see the vcontroller on windows 10.
Else if you have finished setup (see bellow) and you want to 
publish your TRUDDER to your game as well as the combined pedals, 
it won't work

To map your single pedals instead of the virtual ones to anygame
if you have not published axis for them with MapAxis
You will need to setup them first without this script.

Configure this script to ConfigureStandAlone on settings:
* 1.- Launch the script and your Game
* 2- Set up your pedals
* 3.- Close the game and stop the script
* 4.- Setup this script to ConfigureCombo on settings
* 5.- Launch the script and your Game
* 6.- Setup the combined Axis
* 7.- Close the game and delete the ComboPedalsConfigureStandAlone and ComboPedalsConfigureCombo or alternatively, uncommnent the ComboPedalsConfigured setting on settings
* 8.- Launch the script and the Game 
* 9.- Enjoy!
