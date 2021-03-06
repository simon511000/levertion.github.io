---
title: Remove Vanilla Advancements
excerpt: "Two methods of removing vanilla Advancements, and how this works"
categories: 
  - advancements
tags:
  - Vanilla 
  - Mapmaking
  - Video Production
  - Minecraft
  - Advancements
---
# Introduction  
For a lot of Minecraft content apart from the vanilla survival experience, the vanilla advancements take away from the professionalism rather than add to the experience of the content. This is especially important for map-making and tutorial video production, when it removes from immersion because of unneeded toasts.  
Luckily, vanilla Minecraft has multiple methods to remove these advancements. This also stops the gaining of recipes when collecting items.   
# Method 1 (Overwrite all)
## [Download](https://github.com/Levertion/remove-advancements/releases/download/Overwite-allv1.1/remove-advancements.zip)    
### Installation  
Extract the zip from the link above into your world's data folder. This should be the advancements folder rather than the remove-advancements folder.  
## Explanation
*This is my preferred method:*  
For each advancement, it replaces the content with:  
```json
{"criteria":{
  "impossible":{
    "trigger":"minecraft:impossible"
}}}
```
This is because when Minecraft detects that there is an advancement with the same filename as one of the vanilla ones in the map, it uses that one instead, which can have custom properties. The above json creates an advancement with no display data, so it does not have an icon or display a toast.  
The code used to generate the folder can be found [here](https://github.com/Levertion/remove-advancements/blob/overwrite-all/noadvancements.py). This is a [python](https://www.python.org/) script mostly based on [this stackoverflow answer](https://stackoverflow.com/a/19308592) and extracted the original advancements with [7-zip](http://www.7-zip.org/) from the Minecraft 1.12 client jar  
# Method 2 (Create invalid roots)
This method is documented [here](https://www.reddit.com/r/MinecraftCommands/comments/6fvcdj/empty_advancements/dim8lq2/?st=j6qkunj1&sh=b85d431d) by [/u/makluss](https://www.reddit.com/user/Mlakuss) on Reddit, as well as a discussion of the advantages and disadvantages of both methods.  
# Credit  
You are not required to credit me if you use this download. However, if you wish to, please make sure to give a link to either the home page ({{site.url}}), or this page ({{ page.url | absolute_url }}), as well as my twitter [@levertionmc](https://twitter.com/LevertionMC)
