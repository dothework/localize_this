## Localization Guide

__NOTE: Translate from en-US to jp-JP, es-MX,and es-ES.__

### Getting Sample output from the current porcess
You can try it here [https://xrzemepq90.execute-api.us-east-1.amazonaws.com/default/ask-custom-AppleRSS-button?skillId=de_apple-music_coming-soon&locale=en-GB](https://xrzemepq90.execute-api.us-east-1.amazonaws.com/default/ask-custom-AppleRSS-button?skillId=de_apple-music_coming-soon&locale=en-GB)

Locales you can use today
- en-CA
- en-GB
- en-US
- fr-FR
- de-DE

You can also edit the skill id to get to different data. You have the pattern in the appleFeeds.json. The counntry code list is the standard abbreviations. 

### Localize Apple Feed strings in appleFeeds.json
__Localize These Fields:__
- name
- summary
- vuiPreamble
- feedTitle

NOTE: The feeds can be viewed here [https://rss.itunes.apple.com](https://rss.itunes.apple.com)

### Localize strings in skill.json
Only the description field needs to be localized. 

__Leave the DESCRIPTION word in place. That is replaced with the summary data from appleFeeds.json__

### Localize this string
'I am unable to get the listing for you, as there is an issue with the feed from Apple. Please check back soon for updates.'

### Localize this computed string
The string below merges static text, data from the feed, and a calculated counter to determine the entires position in the list, ie: one, two, three...  

Localize the text in the double quotes, or even rewrite it for greater clarity.

" Number " + `<say-as interpret-as="number">${counter}</say-as>` + " is: "  + itemName + ", by " + artistName

Here is the specail case text for the tenth/last entry in the list.

" And number " + `<say-as interpret-as="number">${counter}</say-as>` + " is: "  + itemName + ", by " + artistName
