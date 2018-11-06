##Localization Guide

NOTE: Translate from en-US to de-DE and, if possible, fr-FR. 

###Localize Apple Feed strings in appleFeeds.json
_Localize These Fields:_
- name
- summary
- vuiPreamble
- feedTitle

NOTE: The feeds can be viewed here [https://rss.itunes.apple.com](https://rss.itunes.apple.com)

###Localize strings in skill.json
Only the description field needs to be localized. 

_Leave the DESCRIPTION word in place. That is replaced with the summary data from appleFeeds.json_

###Localize this array
['January','February','March','April','May','June','July','August','September','October','November','December']

###Localize this string
'I am unable to get the listing for you, as there is an issue with the feed from Apple. Please check back soon for updates.'

###Localize this computed string
The string below merges static text, data from the feed, and a calculated counter to determine the entires position in the list, ie: one, two, three...  

Localize the text in the double quotes, or even rewrite it for greater clarity.

" Number " + `<say-as interpret-as="number">${counter}</say-as>` + " is: "  + itemName + ", by " + artistName

Here is the specail case text for the tenth/last entry in the list.

" And number " + `<say-as interpret-as="number">${counter}</say-as>` + " is: "  + itemName + ", by " + artistName
