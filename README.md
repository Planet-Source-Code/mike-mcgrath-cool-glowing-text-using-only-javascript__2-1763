<div align="center">

## Cool Glowing Text Using only Javascript\!


</div>

### Description

This code is a simple demonstration of a text that fades in and fades out using only Javascript. You can customize this code to display your own custom messages. Cool!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Mike McGrath](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/mike-mcgrath.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__2-75.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/mike-mcgrath-cool-glowing-text-using-only-javascript__2-1763/archive/master.zip)





### Source Code

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
<TITLE>Glowing Text Javascript &copy; Mike McGrath UK 1999</TITLE>
<SCRIPT LANGUAGE="javascript" TYPE="text/javascript">
<!-- Original: Mike McGrath (mike_mcgrath@lineone.net) -->
<!-- Web Site: http://website.lineone.net/~mike_mcgrath -->
<!--
var loop = true;  // toggle on/off
var xpos = "20";  // left distance
var ypos = "30";  // top distance
var wide = "325";  // layer width
var rate = "250";  // change speed
var tnum = "1";
var t = new Array();
t[1] = ".....Welcome to this .....";
t[2] = "...Simple Demonstration...";
t[3] = ".... It\'s Just Javascript !";
var cnum = "1";
var c = new Array();
c[1] = "black";
c[2] = "gray";
c[3] = "silver";
c[4] = "whitesmoke";
c[5] = "white";
c[6] = "white";
c[7] = "white";
c[8] = "whitesmoke";
c[9] = "silver";
c[10] = "gray";
c[11] = "black";
c[12] = "black";
if(document.layers)document.write("<layer name='hi' Left='"+xpos+"' Top='"+ypos+"' Width='"+wide+"'></layer>");
if(document.all)document.write("<div id='hi' style='position:absolute;left:"+xpos+";top:"+ypos+";width:"+wide+"'></div>");
function glow()
{
	if(document.layers)
	{
		if(tnum < t.length)
		{
			if(cnum < c.length-1)
			{
				document.layers["hi"].document.write("<font size=5 color='"+c[cnum]+"'>"+t[tnum]+"</font>");
				document.layers["hi"].document.close();
				cnum++;
			}
			else
			{
    cnum = 1;
			 tnum++;
    if(loop)
    {
     if(tnum == t.length) tnum = 1;
    }
			}
 		setTimeout("glow()",rate);
		}
  else
  {
   document.layers["hi"].document.write("");
	  document.layers["hi"].document.close();
  }
	}
 if(document.all)
	{
	 if(tnum < t.length)
		{
			if(cnum < c.length-1)
			{
				document.all("hi").innerHTML = "<font size=5 color='"+c[cnum]+"'>"+t[tnum]+"</font>";
				cnum ++;
			}
			else
			{
			 cnum = 1;
    tnum ++;
    if(loop)
    {
     if(tnum == t.length) tnum = 1;
    }
			}
	  setTimeout("glow()",rate);
		}
  else document.all("hi").innerHTML = "";
	}
}
onload=glow;
//-->
</SCRIPT>
</HEAD>
<BODY BGCOLOR="black">
</BODY>
</HTML>
```

