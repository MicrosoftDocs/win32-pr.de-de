---
title: Verwenden von Skripts zum Steuern von URL-Flipping
description: Verwenden von Skripts zum Steuern von URL-Flipping
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, webbasierte Präsentationen
- Windows Media Player-Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement, webbasierte Präsentationen
- ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player, URL-kippen
- Windows Media Player-Objektmodell, URL-kippen
- Objektmodell, URL-kippen
- Windows Media Player Mobile, URL-kippen
- Windows Media Player ActiveX-Steuerelement, URL-kippen
- Windows Media Player Mobile ActiveX-Steuerelement, URL-kippen
- ActiveX-Steuerelement, URL-kippen
- Webbasierte Präsentationen, URL-kippen
- Erstellen von webbasierten Präsentationen, URL-kippen
- URL-kippen
- Windows Media Player, Rich-Media-Streaming
- Windows Media Player-Objektmodell, Rich-Media-Streaming
- Objektmodell, Rich-Media-Streaming
- Windows Media Player Mobile, Rich-Media-Streaming
- Windows Media Player ActiveX-Steuerelement, Rich-Media-Streaming
- Windows Media Player Mobile ActiveX-Steuerelement, Rich-Media-Streaming
- ActiveX-Steuerelement, Rich-Media-Streaming
- Webbasierte Präsentationen, Rich-Media-Streaming
- Erstellen von webbasierten Präsentationen, Rich-Media-Streaming
- Rich-Media-Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "104388840"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="4ea48-130">Verwenden von Skripts zum Steuern von URL-Flipping</span><span class="sxs-lookup"><span data-stu-id="4ea48-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="4ea48-131">Wenn ein Benutzer eine Verbindung mit einem Rich-Media-Stream herstellt, während der Stream bereits ausgeführt wird, ist es möglich, dass die streamingwebseite angezeigt wird, bevor alle Elemente eingetroffen sind und zwischengespeichert wurden, wenn Windows Media Player die URL automatisch aufruft.</span><span class="sxs-lookup"><span data-stu-id="4ea48-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="4ea48-132">Wenn dies der Fall ist, wird dem Benutzer eine leere oder unvollständige Webseite angezeigt, bis der nächste Satz von Daten im Cache ankommt.</span><span class="sxs-lookup"><span data-stu-id="4ea48-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="4ea48-133">Sie können vermeiden, dass eine leere oder unvollständige Webseite angezeigt wird, indem Sie die URL mithilfe eines Skripts aufrufen, anstatt Windows Media Player die automatische durchführen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="4ea48-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="4ea48-134">Auf diese Weise können Sie den ersten URL-Flip ignorieren und dann nachfolgende URLs mithilfe von Skriptcode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4ea48-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="4ea48-135">In diesem Abschnitt wird davon ausgegangen, dass Sie HTML mit dem Windows Media Encoder 9-Reihe-SDK streamen und den HTML-Stream wiederholen.</span><span class="sxs-lookup"><span data-stu-id="4ea48-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="4ea48-136">Zunächst müssen Sie eine Frameset-Webseite erstellen, die den Frame mit dem eingebetteten Player und dem Frame enthält, in dem der Streaming-HTML-Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea48-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="4ea48-137">Bei jedem dieser beiden Frames wird anfänglich eine separate Webseite angezeigt, sodass Sie insgesamt drei Webseiten erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ea48-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="4ea48-138">Der folgende Beispielcode veranschaulicht die Frameset-Webseite:</span><span class="sxs-lookup"><span data-stu-id="4ea48-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="4ea48-139">Im vorherigen Beispiel für eine Webseite werden zwei Frames integriert.</span><span class="sxs-lookup"><span data-stu-id="4ea48-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="4ea48-140">Der erste Frame wird in der linken Hälfte des Browserfensters angezeigt und zeigt die Webseite mit dem Namen Einbettungs \_player.htm an.</span><span class="sxs-lookup"><span data-stu-id="4ea48-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="4ea48-141">Der folgende Beispielcode erstellt diese Webseite:</span><span class="sxs-lookup"><span data-stu-id="4ea48-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="4ea48-142">Der zweite Frame im Frameset wird in der rechten Hälfte des Browserfensters angezeigt und zeigt eine Webseite mit dem Namen "blank.htm" an.</span><span class="sxs-lookup"><span data-stu-id="4ea48-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="4ea48-143">Der folgende Beispielcode erstellt diese Webseite:</span><span class="sxs-lookup"><span data-stu-id="4ea48-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="4ea48-144">Wenn die Frameset-Seite im Browser geladen wird, zeigt der linke Rahmen den eingebetteten Player an, und der Rechte Rahmen zeigt den Text "wird geladen..." , um den Benutzer darüber zu informieren, dass weitere Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4ea48-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="4ea48-145">Wenn der erste URL-Skript Befehl aus dem HTML-Stream eintrifft, ändert der Ereignishandler einfach den Wert des **booleschen** Flags.</span><span class="sxs-lookup"><span data-stu-id="4ea48-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="4ea48-146">Wenn jeder nachfolgende URL-Skript Befehl aus dem HTML-Stream eintrifft, lädt das Skript im Ereignishandler die neue URL in den Frame mit dem Namen "Content", und die gesamte Webseite wird in dem Frame angezeigt, der sich in der rechten Hälfte des Browserfensters befindet.</span><span class="sxs-lookup"><span data-stu-id="4ea48-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="4ea48-147">Weitere Informationen zum Streaming von HTML mithilfe von Windows-Medien finden Sie im Windows Media Encoder SDK.</span><span class="sxs-lookup"><span data-stu-id="4ea48-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ea48-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ea48-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea48-149">**Rich-Media-Streaming**</span><span class="sxs-lookup"><span data-stu-id="4ea48-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="4ea48-150">**URL-Flipping**</span><span class="sxs-lookup"><span data-stu-id="4ea48-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




