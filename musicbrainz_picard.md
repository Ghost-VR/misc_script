# MusicBrainz Picard

## File naming script
```
$if2(%albumartist%,%artist%)/
$if(%albumartist%,\(%originalyear%\) %album%/,)
$if($gt(%totaldiscs%,1),%discnumber%-,)
$if($and(%albumartist%,%tracknumber%),$num(%tracknumber%,2) ,)
$if(%_multiartist%,$left(%artist%, 10) - ,)
%title%
```