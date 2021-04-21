# cbpp-icon-theme
Default icon themes for use with CrunchBangPlusPlus.

Really it's just a copy of Faenza-Darker -> Faenza-Dark -> Faenza, then
greyscaled /places with:

```
for i in $(find . ! -type l); do echo $i; mogrify -colorspace gray $i; done
for i in $(find . ! -type l); do echo $i; inkscape -f $i --verb EditSelectAll --verb org.inkscape.color.desaturate.noprefs --verb FileSave --verb FileQuit; done
```
