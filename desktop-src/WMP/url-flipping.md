---
title: URL-Flipping
description: URL-Flipping
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2019
ms.locfileid: "103714723"
---
# <a name="url-flipping"></a><span data-ttu-id="46d11-120">URL-Flipping</span><span class="sxs-lookup"><span data-stu-id="46d11-120">URL Flipping</span></span>

<span data-ttu-id="46d11-121">Die Verwendung von Webseiten für Folien anzeigen wird als URL-Flipping bezeichnet und automatisch von Windows Media Player behandelt, wenn URL-Skript Befehle gefunden werden, die in den digitalen Mediendaten Strom eingebettet sind, der wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46d11-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="46d11-122">Sie können einen Zielframe für Ihre Seiten in jedem Skript Befehl angeben. Sie können ihn auch angeben, indem Sie die Eigenschaft **Settings. defaultframe** festlegen.</span><span class="sxs-lookup"><span data-stu-id="46d11-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="46d11-123">Sie können diese Eigenschaft im Skriptcode oder mit einem param-Element innerhalb des Object-Elements festlegen, das das Windows Media Player-Steuerelement einbettet.</span><span class="sxs-lookup"><span data-stu-id="46d11-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="46d11-124">Sie können die URL-Skript Befehle in Ihrem JScript-Code genauso wie benutzerdefinierte Skript Befehle verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="46d11-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="46d11-125">Wenn Sie möchten, dass das Windows Media Player-Steuerelement URL-Skript Befehle ignoriert, damit Sie sie vollständig selbst verarbeiten können, legen Sie die *Einstellungen* fest. die **invokeurls** -Eigenschaft ist entweder im Skriptcode oder bei Verwendung eines Param-Elements wie zuvor beschrieben zu false.</span><span class="sxs-lookup"><span data-stu-id="46d11-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="46d11-126">Das folgende Beispiel veranschaulicht ein typisches Frameset für das URL-Flipping.</span><span class="sxs-lookup"><span data-stu-id="46d11-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="46d11-127">Erstellen Sie zunächst eine Seite, die das Frameset beschreibt:</span><span class="sxs-lookup"><span data-stu-id="46d11-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="46d11-128">Erstellen Sie als nächstes die player.html-Datei, auf die im Frameset verwiesen wird, indem Sie den folgenden Code verwenden (es wird angenommen, dass die Datei "Video. wmv" im gleichen Verzeichnis wie die HTML-Dateien vorhanden ist):</span><span class="sxs-lookup"><span data-stu-id="46d11-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="46d11-129">Wenn Ihre Webseiten so klein sind, dass Sie schnell geladen werden können, genügt diese Einrichtung ggf. für Ihre Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="46d11-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="46d11-130">Wenn andererseits ihre Webseiten komplex sind, kann das umfangreiche Medien Streaming abhängig von der Verbindungsgeschwindigkeit Ihrer Zielgruppe effektiver sein.</span><span class="sxs-lookup"><span data-stu-id="46d11-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="46d11-131">Das URL-kippen funktioniert nicht ordnungsgemäß mit Seiten, die im Netscape Navigator angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="46d11-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="46d11-132">Anstatt in dem von **defaultframe** angegebenen Frame angezeigt zu werden, zeigt jeder im Navigator empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an.</span><span class="sxs-lookup"><span data-stu-id="46d11-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="46d11-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46d11-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d11-134">**Erstellen von Web-Based Präsentationen**</span><span class="sxs-lookup"><span data-stu-id="46d11-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="46d11-135">**Verwenden von Skripts zum Steuern von URL-Flipping**</span><span class="sxs-lookup"><span data-stu-id="46d11-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




