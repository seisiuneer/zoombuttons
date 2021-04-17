
# zoombuttons

For those of you hosting Zoom sessions, if you are like me, you are often having to copy and paste the same text each week into the chat.  

For example, in John Whelan's "Taking Time" and tune teaching events that I co-host, I periodically post his tip jar and Master Sessions info multiple times over the course of the event.

I've typically done that by keeping a text document open in another window specific for each event, and then manually selecting, copying the text, clicking back into the Zoom chat, and then pasting the text.  

That works OK, but it's very easy to make a mistake during the process.

To help automate this process, I've built a little web-based tool that you are welcome to copy and modify to your own requirements.

It's essentially a button board that copies text onto the clipboard, which you can then paste into the Zoom chat.

# Installing

Since it's a web page, you'll either need to host it somewhere, or could just run it locally from your computer.  

I've tested it with Firefox and Chrome on Windows and on iOS Safari, so should work on Safari on Mac as well.

To modify to your requirements there are two areas, the buttons and the text that is copied to the clipboard by the buttons.

Each button has an onclick handler that calls a function called "copyToClipboard()" that includes the absolute ID of a ul element that in turn contains one or more li elements.

and each button pairs up with a invisible ul tag with the id sent to the copyToClipboard() function:
    
copyToClipboard() reads the contents of the ul, formats the text with each li element turned into a line of text, creates a temporary text area, pastes the text into the text area, then copies it to the system clipboard, then destroys the text area.

You should not have to modify this function, only the buttons and ul lists to create your own buttons. 

If you walk through the page, it's very simple to modify or extend to add additional buttons.
