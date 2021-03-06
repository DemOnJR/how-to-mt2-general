This is a revised version of an old thread. Following this How-To, you will have a better customizable solution for the aspect of your quests.

You will be able to choice amongst: quest icon, text color, blink effect (like whisper buttons)

### How To
You just need to replace 2 little things:

In interfaceModule.py, replace BINARY_RecvQuest with:
[interfaceModule.codepart.py](interfaceModule.codepart.py)

In questlib.lua, replace send_letter_ex with:
[questlib.codepart.lua](questlib.codepart.lua)

### Explanation:
- the 2° argument of send_letter_ex will support multiple parameters:

	- green|blue|purple|golden|fucsia|aqua and so on (you can add them in BINARY_RecvQuest by adding new colors 0xFF+#HEX; [Color Picker Online](https://www.w3schools.com/colors/colors_picker.asp))
	- blink (the quest will flash like the whisper messages)
	- ex (a dummy tag to separate it from "info" and "item")

- the 3° argument is the name of the icon to choose, which the current availables are:

	- scroll_open.tga
	- scroll_open_green.tga
	- scroll_open_blue.tga
	- scroll_open_purple.tga
	- scroll_open_golden.tga

### Examples:

- [![Result Label](http://i.imgur.com/3n9yRqF.png)](http://i.imgur.com/3n9yRqF.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "green,blink,ex", "scroll_open_green.tga")```

- [![Result Label](http://i.imgur.com/M8MMP3N.png)](http://i.imgur.com/M8MMP3N.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "blue,blink,ex", "scroll_open_blue.tga")```

- [![Result Label](http://i.imgur.com/gkEolrr.png)](http://i.imgur.com/gkEolrr.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "purple,blink,ex", "scroll_open_purple.tga")```

- [![Result Label](http://i.imgur.com/AH6tgAW.png)](http://i.imgur.com/AH6tgAW.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "golden,blink,ex", "scroll_open_golden.tga")```

- [![Result Label](http://i.imgur.com/7uBSyfS.png)](http://i.imgur.com/7uBSyfS.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "golden,blink,ex", "scroll_open.tga")```

- [![Result Label](http://i.imgur.com/qvhg6Ql.png)](http://i.imgur.com/qvhg6Ql.png)

	```send_letter_ex(localeInfo.LanguageOptionTitle, "golden,blink,ex", "scroll_open_green.tga")```

_Note: As you can imagine, the only limitation is that the color in N won't appear. (it will require additional code and work, so just forget it)_

### Download:
Add metin2_patch_new_questicon in your client.
