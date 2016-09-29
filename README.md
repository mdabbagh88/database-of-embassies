# Database of embassies and consulates

[>>> Click here to see the data or download it (Press "Run" then "Download" then "CSV") <<<](https://query.wikidata.org/#%23Embassies%20and%20consulates%0ASELECT%20DISTINCT%0A%09%28SAMPLE%28%3Fcountry_label%29%20as%20%3Fcountry%29%20%20%20%28SAMPLE%28%3Fcity_label%29%20as%20%3Fcity%29%20%20%20%28SAMPLE%28%3Faddress%29%20as%20%3Faddress%29%20%28SAMPLE%28%3Fcoordinates%29%20as%20%3Fcoordinates%29%0A%09%28SAMPLE%28%3Foperator_label%29%20as%20%3Foperator%29%20%28SAMPLE%28%3Ftype_label%29%20as%20%3Ftype%29%20%20%20%28SAMPLE%28%3Fphone%29%20as%20%3Fphone%29%20%20%20%20%20%28SAMPLE%28%3Femail%29%20as%20%3Femail%29%0A%09%28SAMPLE%28%3Fwebsite%29%20as%20%3Fwebsite%29%20%20%20%20%20%20%20%20%20%28SAMPLE%28%3Fimage%29%20as%20%3Fimage%29%20%20%20%20%20%20%20%3Fwikidata%0A%09%23%28SAMPLE%28%3Ffacebook%29%20as%20%3Ffacebook%29%20%28SAMPLE%28%3Ftwitter%29%20as%20%3Ftwitter%29%20%28SAMPLE%28%3Fyoutube%29%20as%20%3Fyoutube%29%20%28SAMPLE%28%3Finception%29%20as%20%3Finception%29%20%28SAMPLE%28%3FdissolvedOrAbolished%29%20as%20%3FdissolvedOrAbolished%29%0AWHERE%20%7B%0A%09%7B%20%3Fwikidata%20p%3AP31%2Fps%3AP31%2Fwdt%3AP279%2a%20wd%3AQ3917681.%20%7D%20UNION%20%7B%20%3Fwikidata%20wdt%3AP31%20wd%3AQ7843791.%20%7D%20%23%20Embassy%20or%20consulate%0A%09%3Fwikidata%20p%3AP31%2Fps%3AP31%20%3FtypeId.%20%3FtypeId%20rdfs%3Alabel%20%3Ftype_label.%20filter%20%28lang%28%3Ftype_label%29%20%3D%20%22en%22%29.%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP131%2a%2Fwdt%3AP17%20%3FcountryId.%20%3FcountryId%20rdfs%3Alabel%20%3Fcountry_label.%20filter%20%28lang%28%3Fcountry_label%29%20%3D%20%22en%22%29.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP131%20%3FcityId.%20%3FcityId%20rdfs%3Alabel%20%3Fcity_label.%20filter%20%28lang%28%3Fcity_label%29%20%3D%20%22en%22%29.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP969%20%3Faddress.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP625%20%3Fcoordinates.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP137%20%3FoperatorId.%20%3FoperatorId%20rdfs%3Alabel%20%3Foperator_label.%20filter%20%28lang%28%3Foperator_label%29%20%3D%20%22en%22%29.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP1329%20%3Fphone.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP968%20%3Femail.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP856%20%3Fwebsite.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP2013%20%3Ffacebook.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP2002%20%3Ftwitter.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP2397%20%3Fyoutube.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP18%20%3Fimage.%7D%0A%20%20%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP571%20%3Finception.%7D%0A%09OPTIONAL%20%7B%3Fwikidata%20wdt%3AP576%20%3FdissolvedOrAbolished.%7D%0A%7D%20GROUP%20BY%20%3Fwikidata%20ORDER%20BY%20ASC%28%3Fcountry%29%20ASC%28%3Fcity%29%20ASC%28%3Foperator%29%20DESC%28%3Ftype%29)

# Help needed

**Non-developers:** The database is not complete, we need your help to improve it. To add/modify/remove information, please edit the relevant item in [Wikidata](http://wikidata.org) ([example](https://www.wikidata.org/wiki/Q2841718)). If no item is available on Wikidata, please create it, or add it to the city in [Wikivoyage](http://wikivoyage.org) ([example](https://en.wikivoyage.org/wiki/Karachi#Consulates)) if you are not confortable with Wikidata. Thanks!

**Developers:** Take 10 minutes to familiarize yourself with [SPARQL](https://www.wikidata.org/wiki/Wikidata:SPARQL_query_service/queries) then [pick any issue](https://github.com/nicolas-raoul/database-of-embassies/issues) you like :-) Don't hesitate to create other issues to document any problem with the data, or send pull requests to add your custom scripts. Convenient tools: [QuickStatements](https://tools.wmflabs.org/wikidata-todo/quick_statements.php), [Harvest Templates](https://tools.wmflabs.org/pltools/harvesttemplates/).
