# Better Live Routings

Better Live Routings is a Max patch that performs a simple task: route *all* data to/from a pair of MIDI ports on your computer. You open the patch, select your ports, and that's it.

## Why Would I Need This?

There are many reasons why you might need this, but this patch was created to solve a specific problem: there is some bugginess in the behavior of the "Live Routings" feature of the Network MIDI device on OS X (and maybe in rtpMIDI on Windows as well). In my usage of Network MIDI, I've found that some MIDI data somehow doesn't make it through the Live Routings. It seems to get filtered. I don't know how or why, but it's definitely happening.

## Usage

If, like me, you're using this patch as a replacement for using "Live Routings" in networked MIDI, then this is how you use it:

1. Make sure "Live routings" menu in your network MIDI setup is set to blank! Leaving Live routings turned on, when used with this patch as well, will probably cause bad behavior.
2. Open the patch better-live-routings.maxpat. You'll need Max to run it (which you can get for free from Cycling 74 here: )
3. Select your ports in the dropdown menus of the patch. In most setups, you'll select your Network MIDI port in the first "From" dropdown, and your MIDI device output port in the first "To" dropdown. Then select them vice versa in the second set of dropdowns ("From" your MIDI device, and "To" your Network MIDI port)
4. Now you should be in business. The two circles on the right side of the patch are indicators for when MIDI is being received from the chosen MIDI ports.
5. When you close the patch, it will attempt to automatically save your settings to a file called config.json that is in the same folder as better-live-routings.maxpat. That'll save you time the next time around.

Here's an example of how your Live Routings should look on OS X (the lower-right is the important part):

![Live Routings example](https://d2250zc18i5qvg.cloudfront.net/sites/default/files/pages/Screen%20Shot%202015-04-16%20at%204.37.44%20PM.png)

Here's an example of a correct setup of the patch:

![Better Live Routings example](https://d2250zc18i5qvg.cloudfront.net/sites/default/files/pages/Screen%20Shot%202015-04-16%20at%204.43.58%20PM.png)
