# cbpp-icon-theme
Default icon themes for use with CrunchBangPlusPlus.

Really it's just a copy of Faenza-Darker -> Faenza-Dark -> Faenza, then
greyscaled `/places` with:

```
for i in $(find . -type f -name "*.png"); do echo $i; mogrify -colorspace gray $i; done
for i in $(find . -type f -name "*.svg"); do echo $i; inkscape --batch-process --actions="org.inkscape.color.desaturate.noprefs;export-overwrite;export-do;" $i; done
```
