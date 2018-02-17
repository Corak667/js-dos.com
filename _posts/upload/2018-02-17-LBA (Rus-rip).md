---
layout: post
title: LBA
showcase: true
keywords: LBA,pc,game,javscript
description: Play in the LBA in browser.
permalink: LBA/
---

Play in the legendary game **LBA** in browser. (Uploaded by: caiiiycuk)

{% include dosbox.html version="2" width="640" height="480" bg="LBA.png" game="LBA" archive="/cdn/upload/LBA.zip" exe="./LBA.EXE" %}

<!--more-->

{% include details.html name="LBA" createdat="1994" publisher="Electronic Arts" category="Adventure" %}



### Source

{% highlight html linenos %}
<!doctype html>
<html lang="en-us">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>LBA</title>
    <style type="text/css">
      .dosbox-container { width: 640px; height: 400px; }
      .dosbox-container > .dosbox-overlay { background: url(https://js-dos.com/cdn/LBA.png); }
    </style>
  </head>
  <body>
    <div id="dosbox"></div>
    <br/>
    <button onclick="dosbox.requestFullScreen();">Make fullscreen</button>
    
    <script type="text/javascript" src="https://js-dos.com/cdn/js-dos-api.js"></script>
    <script type="text/javascript">
      var dosbox = new Dosbox({
        id: "dosbox",
        onload: function (dosbox) {
          dosbox.run("upload/LBA.zip", "./F117.COM");
        },
        onrun: function (dosbox, app) {
          console.log("App '" + app + "' is runned");
        }
      });
    </script>
  </body>
</html>
{% endhighlight %}
