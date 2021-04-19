---
title: Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird
description: Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- Windows Media Player ActiveX-Steuerelement, invokeurls-Eigenschaft
- Windows Media Player Mobile ActiveX-Steuerelement, invokeurls (Eigenschaft)
- Einbettungen, Webseiten
- Aufbetten von Webseiten, invokeurls (Eigenschaft)
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, invokeurls (Eigenschaft)
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106337622"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="23c32-122">Verwenden der invokeurls-Eigenschaft in einer Webseite, die von Firefox angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="23c32-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="23c32-123">Einige Mediendateien enthalten eingebettete URLs, für die Windows Media Player Webseiten in einem Webbrowser Fenster oder-Frame anzeigt, wenn die Mediendatei abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="23c32-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="23c32-124">In Windows Internet Explorer können Sie mit der Eigenschaft [Settings. invokeurls](settings-invokeurls.md) angeben, ob Seiten für eingebettete URLs angezeigt werden, und Sie können mit der Eigenschaft [Settings. defaultframe](settings-defaultframe.md) einen Frame zum Anzeigen solcher Seiten angeben.</span><span class="sxs-lookup"><span data-stu-id="23c32-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="23c32-125">In Firefox sind einige Problem Umgehungen erforderlich, um die **invokeurls** -Eigenschaft festzulegen und einen Frame zum Anzeigen von Seiten für eingebettete URLs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="23c32-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="23c32-126">Festlegen der invokeurls-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="23c32-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="23c32-127">Der Standardwert der **Settings. invokeurls** -Eigenschaft ist true. Wenn Sie also den Wert false festlegen möchten, müssen Sie ihn explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="23c32-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="23c32-128">In Internet Explorer können Sie **invokeurls** in einem param-Element innerhalb des Objekt Elements des Player-Steuer Elements auf false festlegen.</span><span class="sxs-lookup"><span data-stu-id="23c32-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="23c32-129">Das Plug-in für Firefox unterstützt das Festlegen der **invokeurls** -Eigenschaft in einem param-Element nicht.</span><span class="sxs-lookup"><span data-stu-id="23c32-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="23c32-130">Sie können diese Einschränkung umgehen, indem Sie die **invokeurls** -Eigenschaft im Skript festlegen.</span><span class="sxs-lookup"><span data-stu-id="23c32-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="23c32-131">Der folgende Code zeigt, wie die **invokeurls** -Eigenschaft auf einer Webseite, die sowohl von Internet Explorer als auch von Firefox angezeigt werden kann, auf false festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="23c32-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="23c32-132">Anzeigen von Webseiten in einem Frame</span><span class="sxs-lookup"><span data-stu-id="23c32-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="23c32-133">Eine Mediendatei kann URLs enthalten, in denen Webseiten in einem Browserfenster oder-Frame angezeigt werden, während die Mediendatei wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="23c32-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="23c32-134">In Internet Explorer können Sie die Eigenschaft [Settings. defaultframe](settings-defaultframe.md) verwenden, um den Frame anzugeben, in dem diese Seiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="23c32-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="23c32-135">Wenn Sie die **defaultframe** -Eigenschaft nicht festlegen, werden URLs in einem separaten Fenster des Standard Browsers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="23c32-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="23c32-136">Das Firefox-Plug-in unterstützt jedoch nicht die **Settings. defaultframe** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="23c32-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="23c32-137">Um diese Einschränkung zu umgehen, legen Sie die Eigenschaft **Settings. invokeurls** auf false fest, und schreiben Sie einen [ScriptCommand](player-player-scriptcommand.md) -Ereignishandler, der den Speicherort des Zielframes festlegt.</span><span class="sxs-lookup"><span data-stu-id="23c32-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="23c32-138">Das folgende Beispiel, das in Internet Explorer und Firefox funktioniert, veranschaulicht diese Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="23c32-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="23c32-139">Angenommen, die im Beispiel gezeigte Webseite wird in Frames 0 angezeigt, \[ \] und Sie möchten, dass die Seite der URL in Frames \[ 1 angezeigt wird \] .</span><span class="sxs-lookup"><span data-stu-id="23c32-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="23c32-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23c32-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c32-141">**Verwenden des Windows Media Player-Steuer Elements mit Firefox**</span><span class="sxs-lookup"><span data-stu-id="23c32-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




