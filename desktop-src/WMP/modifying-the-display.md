---
title: Ändern der Anzeige
description: Ändern der Anzeige
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Media Metadatei-Wiedergabelisten, Ändern von anzeigen
- Wiedergabelisten, Ändern von anzeigen
- Metadatei-Wiedergabelisten, Ändern von anzeigen
- Windows Media Metadatei-Wiedergabelisten, Änderung anzeigen
- Wiedergabelisten, Änderung anzeigen
- Metadatei-Wiedergabelisten, Änderung anzeigen
- Windows Media Player, Änderung anzeigen
- Windows Media Player, Ändern von anzeigen
- Windows Media Player, Texteigenschaften
- Windows Media Player, Bildeigenschaften
- Eigenschaften von Windows Media Player, morumfo
- Windows Media Player, abstrakter Text
- Moreingefo-Eigenschaften
- Abstrakter Text
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036748"
---
# <a name="modifying-the-display"></a><span data-ttu-id="62f78-117">Ändern der Anzeige</span><span class="sxs-lookup"><span data-stu-id="62f78-117">Modifying the Display</span></span>

<span data-ttu-id="62f78-118">Wiedergabelisten können die Windows Media Player-Benutzeroberfläche auf vier verschiedene Arten ändern:</span><span class="sxs-lookup"><span data-stu-id="62f78-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="62f78-119">Text Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-119">Text properties</span></span>
-   <span data-ttu-id="62f78-120">Image-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-120">Image properties</span></span>
-   <span data-ttu-id="62f78-121">Moreingefo-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-121">MOREINFO properties</span></span>
-   <span data-ttu-id="62f78-122">Abstrakter Text</span><span class="sxs-lookup"><span data-stu-id="62f78-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="62f78-123">Text Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-123">Text properties</span></span>

<span data-ttu-id="62f78-124">Windows Media Player ermöglicht das Anzeigen von Text für Titel, Autor, Copyright und Beschreibungs Metadaten.</span><span class="sxs-lookup"><span data-stu-id="62f78-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="62f78-125">Clip-Metadaten können aus dem Stream oder der Mediendatei stammen, oder Sie können aus einer Wiedergabeliste stammen.</span><span class="sxs-lookup"><span data-stu-id="62f78-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="62f78-126">Metadaten anzeigen stammt aus der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="62f78-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="62f78-127">Im Allgemeinen sind Wiedergabelisten eine bessere Methode, Texteigenschaften an Windows-Media Player zu übergeben, insbesondere, wenn sich Textelemente wahrscheinlich ändern.</span><span class="sxs-lookup"><span data-stu-id="62f78-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="62f78-128">Es ist einfacher, Text in einer Wiedergabeliste zu bearbeiten, als eine Mediendatei neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62f78-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="62f78-129">Und da aus einer Wiedergabeliste gelesene Eigenschaften die in der Mediendatei enthaltenen Eigenschaften überschreiben, können Sie den Anzeige Text einfach aktualisieren, indem Sie den neuen Text der entsprechenden Eigenschaft in einer Wiedergabeliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="62f78-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="62f78-130">Im folgenden Beispiel überschreibt der Text der Titel-und Author-Metadaten in der Wiedergabeliste den Titel und den Autor Text, der in der Mediendatei Sample. WMA enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="62f78-131">Der **Beschreibungs** Text wird aus einer Windows-Mediendatei abgerufen, auf die in einem **Entry** -Element verwiesen wird, es sei denn, es gibt ein **abstraktes** Element in einer</span><span class="sxs-lookup"><span data-stu-id="62f78-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="62f78-132">Wenn **abstrakter** Text vorhanden ist, wird er angezeigt, und der **Beschreibungs** Text wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="62f78-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="62f78-133">Image-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-133">Image properties</span></span>

<span data-ttu-id="62f78-134">Banner Bilder können der Benutzeroberfläche von Windows Media Player hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="62f78-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="62f78-135">Die Grafik kann für Werbung, Bereitstellung von Informationen und Bereitstellung von Zugriff auf Websites verwendet werden, um einige Möglichkeiten zu benennen.</span><span class="sxs-lookup"><span data-stu-id="62f78-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="62f78-136">Verwenden Sie das **Banner** -Element, um ein Grafik Bild (32 Pixel hoch um 194 Pixel breit) für die Anzeige durch Windows Media Player anzugeben.</span><span class="sxs-lookup"><span data-stu-id="62f78-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="62f78-137">Die Grafik wird unterhalb der Videoinhalte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="62f78-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="62f78-138">Ein Link kann dem Banner mithilfe des untergeordneten **Morein FO** -Elements hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="62f78-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="62f78-139">Eine QuickInfo kann von einem **abstrakten** Element innerhalb des Gültigkeits Bereichs des **Banner** Elements definiert werden.</span><span class="sxs-lookup"><span data-stu-id="62f78-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="62f78-140">Jeder definierte QuickInfo-Text kann angezeigt werden, indem der Mauszeiger über der Banner Grafik angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="62f78-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="62f78-141">Wenn Sie die Banner Grafik mit dem Mauszeiger auswählen, wird ein beliebiger Hyperlink aktiviert, der mit dem Element **Moran FO** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="62f78-142">Das bevorzugte **Banner** Grafikformat ist das GIF-Format.</span><span class="sxs-lookup"><span data-stu-id="62f78-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="62f78-143">Das JPG-Format kann verwendet werden, wenn die Grafik ordnungsgemäß formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="62f78-144">Das vorherige Beispiel veranschaulicht die Verwendung des **Banner** -Elements.</span><span class="sxs-lookup"><span data-stu-id="62f78-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="62f78-145">**Banner** Bilder werden bei DRM-Dateien nicht unterstützt, oder wenn Windows Media Player in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="62f78-146">Weitere Informationen zu Banner finden Sie unter [benutzerdefinierte Grafiken in Windows Media Player](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="62f78-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="62f78-147">Moreingefo-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62f78-147">MOREINFO properties</span></span>

<span data-ttu-id="62f78-148">Text-und Bildbereiche der Benutzeroberfläche können URLs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="62f78-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="62f78-149">Während der Wiedergabe können Benutzer einen dieser Abschnitte auswählen, um eine Verbindung mit der zugeordneten URL in Ihrem Webbrowser herzustellen.</span><span class="sxs-lookup"><span data-stu-id="62f78-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="62f78-150">Beispielsweise können Sie die Website eines Werbe einbilds wie im folgenden Code Ausschnitt gezeigt einem Werbebanner Bild zuordnen.</span><span class="sxs-lookup"><span data-stu-id="62f78-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="62f78-151">Abstrakter Text</span><span class="sxs-lookup"><span data-stu-id="62f78-151">ABSTRACT text</span></span>

<span data-ttu-id="62f78-152">Der **abstrakte** Text wird verwendet, um eine kurze Popup Beschreibung der Text-oder Bildbereiche der Benutzeroberfläche anzuzeigen, der er zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="62f78-153">Wenn der Mauszeiger während der Wiedergabe auf einen dieser Bereiche zeigt, wird neben dem Mauszeiger eine QuickInfo mit dem **abstrakten** Text angezeigt, der dem Bereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="62f78-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="62f78-154">Der **abstrakte** Text wird aus einer Metadatei abgerufen und mit dem **abstrakten** Element definiert.</span><span class="sxs-lookup"><span data-stu-id="62f78-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="62f78-155">Das **abstrakte** Element kann ein untergeordnetes Element eines- **Eintrags** oder eines **Banner** -Elements sein.</span><span class="sxs-lookup"><span data-stu-id="62f78-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f78-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62f78-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f78-157">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="62f78-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="62f78-158">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="62f78-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="62f78-159">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="62f78-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="62f78-160">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="62f78-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




