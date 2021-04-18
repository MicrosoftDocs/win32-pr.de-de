---
title: Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite
description: Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Objektmodell, Einbetten des ActiveX-Steuer Elements
- Objektmodell, Einbetten des ActiveX-Steuer Elements
- Windows Media Player Mobile, Einbetten des ActiveX-Steuer Elements
- Windows Media Player ActiveX-Steuerelement, einbetten
- Windows Media Player Mobile ActiveX-Steuerelement, einbetten
- ActiveX-Steuerelement, einbetten
- Windows Media Player ActiveX-Steuerelement, Webseiten
- Windows Media Player Mobile ActiveX-Steuerelement, Webseiten
- ActiveX-Steuerelement, Webseiten
- Windows Media Player, Firefox
- Windows Media Player-Objektmodell, Firefox
- Objektmodell, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX-Steuerelement, Firefox
- Windows Media Player Mobile ActiveX-Steuerelement, Firefox
- ActiveX-Steuerelement, Firefox
- Firefox, Informationen zum Einbetten von Webseiten
- Einbettungen, Webseiten
- Einbettung von Webseiten, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "106338023"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="76733-123">Einbetten des Player-Steuer Elements in eine von Firefox angezeigte Webseite</span><span class="sxs-lookup"><span data-stu-id="76733-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="76733-124">Wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten möchten, die von einem Firefox-Browser angezeigt werden kann, erstellen Sie ein Objekt Element oder ein Einbettungs Element, das einen der folgenden MIME-Typen als **Type** -Attribut aufweist:</span><span class="sxs-lookup"><span data-stu-id="76733-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="76733-125">Anwendung/x-MS-WMP</span><span class="sxs-lookup"><span data-stu-id="76733-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="76733-126">Anwendung/ASX</span><span class="sxs-lookup"><span data-stu-id="76733-126">application/asx</span></span>
-   <span data-ttu-id="76733-127">Video/x-ms-ASF-Plugin</span><span class="sxs-lookup"><span data-stu-id="76733-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="76733-128">Application/x-Mplayer2</span><span class="sxs-lookup"><span data-stu-id="76733-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="76733-129">Video/x-ms-ASF</span><span class="sxs-lookup"><span data-stu-id="76733-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="76733-130">Video/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="76733-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="76733-131">Audiodatei/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="76733-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="76733-132">Audiodatei/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="76733-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="76733-133">Video/x-ms-WMV</span><span class="sxs-lookup"><span data-stu-id="76733-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="76733-134">Video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="76733-134">video/x-ms-wvx</span></span>

<span data-ttu-id="76733-135">Der bevorzugte MIME-Typ ist "application/x-MS-WMP".</span><span class="sxs-lookup"><span data-stu-id="76733-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="76733-136">In den folgenden Beispielen wird veranschaulicht, wie das Player-Steuerelement mit einem Object-Element oder einem Einbettungs Element eingebettet wird.</span><span class="sxs-lookup"><span data-stu-id="76733-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



<span data-ttu-id="76733-137">Die vorangehenden Beispiele funktionieren in Firefox, aber nicht in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="76733-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="76733-138">Wenn Sie das Player-Steuerelement in eine Webseite einbetten möchten, die von Internet Explorer angezeigt werden kann, müssen Sie ein Object-Element erstellen, dessen **ClassID-** Attribut auf die Klassen-ID des Windows Media Player-Steuer Elements festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76733-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="76733-139">Im folgenden Beispiel wird gezeigt, wie Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, die sowohl von Internet Explorer als auch von Firefox richtig angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="76733-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="76733-140">Skript auf der Seite erkennt den Browsertyp und generiert das entsprechende Objekttag.</span><span class="sxs-lookup"><span data-stu-id="76733-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="76733-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76733-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76733-142">**Verwenden des Windows Media Player-Steuer Elements mit Firefox**</span><span class="sxs-lookup"><span data-stu-id="76733-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




