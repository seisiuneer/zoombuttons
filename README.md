
# zoombuttons

For those of you hosting Zoom sessions, if you are like me, you are often having to copy and paste the same text each week into the chat for tunes or recurring event links.  

I had initially done that by keeping a text document open in another window specific for each event, and then manually selecting, copying the text, clicking back into the Zoom chat, and then pasting the text.

That works OK, but it's very easy to make a mistake during the process.

To help automate this process, during the 2020 COVID shutdowns I built a little web-based tool that you are welcome to copy and modify to your own requirements.

It's essentially a button board that copies text onto the clipboard, which you can then paste into the Zoom chat.

Any tunes added to the #tunes div will automatically be alphabetized and will include alphabetic headers for each letter.

Other than including jQuery, the utility is completely self-contained.

# Installing

Since it's a web page, you'll either need to host zoombuttons.html somewhere, or could just run it locally from your computer.  

I've tested it with Firefox and Chrome on Windows and on iOS Safari, so should work on Safari on Mac as well.

# Customization 
```html
HOW TO ADD A NEW ZOOM BUTTON

Each button is made from two matching parts:

1. A <button> that the user sees and clicks.
2. A hidden <ul> list immediately after the button that contains
 the text that will be copied to the clipboard.

Example:

<button onclick="copyToClipboard('#mynewitem')">My New Button</button>
<ul id="mynewitem">
	<li>This is the first line copied to the clipboard.</li>
	<li></li>
	<li>This is a new paragraph after a blank line.</li>
	<li>https://example.com</li>
</ul>

Important details:

- The button's copyToClipboard('#mynewitem') value must match
the <ul id="mynewitem"> value exactly.

- Use a unique ID for each item. Do not reuse an ID that is
already used elsewhere in the file.

- Put each line of copied text inside its own <li>...</li>.

- Use an empty <li></li> when you want a blank line in the
copied text.

- Add normal general-purpose buttons in the main button area.

- Add tune buttons inside <div id="tunes">. Tune buttons are
automatically sorted alphabetically when the page loads.

- The search box searches only the visible button titles, not
the hidden copied text inside the <ul> lists.
```

