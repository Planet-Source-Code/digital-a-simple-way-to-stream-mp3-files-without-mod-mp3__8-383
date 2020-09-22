<div align="center">

## a simple way to stream mp3 files without mod\_mp3


</div>

### Description

This code makes it possible for you to stream any mp3 file on the internet. It does NOT need mod_mp3. It's complete, and ready to go.
 
### More Info
 
$loc == the location of the mp3 file

$Play == "yes" to play the file, or not defined to just prompt

this is stupid easy to use.

the sweet nectar of streaming mp3 music

internal bleeding, spontanious combustion, uncontrolable vomitting


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Digital](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/digital.md)
**Level**          |Advanced
**User Rating**    |3.1 (22 globes from 7 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__8-7.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/digital-a-simple-way-to-stream-mp3-files-without-mod-mp3__8-383/archive/master.zip)

### API Declarations

```
Copyright 2001 - The DE-Network -- Dan Graaff
http://www.de-net.org
```


### Source Code

```
<?
// This Program was written by Digital -- digital@de-net.org
// Any copying without my concent will get you killed by cuban snipers.
// http://www.de-net.org
if (!$Play)
{
?>
<html>
<head>
<title>DE-Network Mp3 Streamer</title>
<style TYPE="text/css">
A:link
{
  COLOR: #00007D;
  TEXT-DECORATION: none
}
A:visited
{
  TEXT-DECORATION: none
}
A:active
{
  TEXT-DECORATION: none
}
A:hover
{
  COLOR: #D90000
}
</style>
</head>
<body topmargin="0" leftmargin="0" bgcolor="#000000" text="#FFFFFF">
<div align="left">
 <table border="0" width="100%" height="100%" cellspacing="0" cellpadding="0" bordercolor="#FFFFFF" bgcolor="#000000">
  <tr>
   <td width="100%" height="50%" valign="bottom">
    <p align="center"><img border="0" src="http://www.de-net.org/insomnia/images/de-network.gif" width="589" height="202"></td>
  </tr>
  <tr>
   <td width="100%" height="48%" valign="top">
   <b>
<form action=<? echo $PHP_SELF; ?> method=POST>
<p align="center">
<font face="Verdana,Arial" size="3" color="#C0C0C0">
Enter the URL of an mp3 file:<br><input type="text" value="<? echo $loc; ?>" name="loc">
<input type="submit" value="Play" name="Play">
<br><br><font size=2>
To use this script seemlessly in your website, pass variables to this script like this:</b><br>
&lt;a href="<i>http://www.de-net.org/audio/?<b>loc</b>=http://wherever.the/mp3/file.is&<b>Play</b>=yes</i>"&gt;<br>Click Here to listen to that one song!&lt;/a&gt;
</font>
</form>
   </td>
  </tr>
  <tr>
   <td width="100%" height="2%" valign="top">
   <p align="center"><b><font face="Verdana,Arial" size="3" color="#808080">Powered
   by <a href="http://www.de-net.org"> The DE-Network</a> | Tool by <a href="http://www.de-net.org/bios?digital"> Digital</a></font></b>
   </td>
  </tr>
 </table>
</div>
</body>
</html>
<?
}
else
{
if (!$loc)
{
     echo "There's no audio file specified...";
     die;
}
$loc = str_replace(" ", "%20",$loc);
Header("Content-Type: audio/x-mpegurl");
echo $loc . "\n"; }
?>
```

