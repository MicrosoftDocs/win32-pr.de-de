---
title: Zugreifen auf Medien
description: Zugreifen auf Medien
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Media Metadatei-Wiedergabelisten, zugreifen auf Medien
- Wiedergabelisten, zugreifen auf Medien
- Metadatendatei-Wiedergabelisten, zugreifen auf Medien
- Windows Media Metadatei-Wiedergabelisten, Medien Zugriff
- Wiedergabelisten, Medien Zugriff
- Metadatei-Wiedergabelisten, Medien Zugriff
- Windows Media Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Windows Media Metadatei-Wiedergabelisten, Einstellungs Dauer
- Wiedergabelisten, Einstellungs Dauer
- Metadatei-Wiedergabelisten, Einstellungs Dauer
- Windows Media Player, zugreifen auf Medien
- Windows Media Player, Medien Zugriff
- Windows Media Player, Steuern der Wiedergabe
- Windows Media Player, Einstellungs Dauer
- Zugreifen auf Medien
- Medien Zugriff
- Steuern der Wiedergabe
- Einstellungs Dauer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338003"
---
# <a name="accessing-media"></a><span data-ttu-id="6b7e5-123">Zugreifen auf Medien</span><span class="sxs-lookup"><span data-stu-id="6b7e5-123">Accessing Media</span></span>

<span data-ttu-id="6b7e5-124">Verwenden Sie Wiedergabelisten, um die Streamingmedien oder Mediendateien anzugeben, die von Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="6b7e5-125">Verwenden Sie das **Entry** -Element, um ein einzelnes Medien Element (eine Mediendatei oder einen Livestream) und alle untergeordneten Elemente (z. b. Bilder, **moreinfo** -Links und **abstrakten** Text) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="6b7e5-126">Verwenden Sie ein **ENTRYREF** -Element, um eine Wiedergabeliste anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="6b7e5-127">Eine Wiedergabeliste kann ein oder mehrere **Entry** -oder **ENTRYREF** -Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="6b7e5-128">Windows Media Player führt eine Wiedergabeliste aus, indem Sie mit dem ersten Eintrag beginnt und dann jeden Eintrag nacheinander wieder gibt, bis die Liste abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="6b7e5-129">Ein **Eintrags** Element kann auf beliebige Medientypen verweisen, die von Windows Media Player wiedergegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="6b7e5-130">Dies schließt nicht nur die Dateien. WMA,. WMV,. ASF und. AVI ein, um nur ein paar, sondern auch Livestreams zu benennen.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="6b7e5-131">Indem Sie eine Reihe von **Entry** -oder **ENTRYREF** -Elementen verwenden, um auf Medieninhalte zu verweisen, können Sie eine Wiedergabeliste verwenden, um einen einzelnen Datenstrom zu senden, der aus mehreren Quellen besteht.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="6b7e5-132">Die referenzierten Streams werden sequenziell abgespielt und als ein fortlaufender Stream des Viewers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="6b7e5-133">Die Wiedergabeliste kann z. b. zwei **Einstiegs** Elemente enthalten: eine Standard Einführung aus einer Windows Media-Datei mit der Erweiterung ". wma" und ein Live-Windows Media-Stream.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="6b7e5-134">Eine Wiedergabeliste darf keine Links zu Mediendateien enthalten, die Inhalte enthalten, die mit verschiedenen Versionen von Digital Rights Management (DRM) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="6b7e5-135">Wenn in einer metadateiwiedergabe Links für Mediendateien mit DRM-Inhalt der Version 1 und Mediendateien vorhanden sind, die mit neueren DRM-Versionen erstellt wurden, gibt Windows Media Player nur den DRM-Inhalt der Version 1 wieder.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="6b7e5-136">Steuern der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="6b7e5-136">Controlling Playback</span></span>

<span data-ttu-id="6b7e5-137">Verwenden Sie Wiedergabelisten, um nicht nur zu steuern, welche Medienclips abgespielt werden, sondern auch welche Teile des Clips abgespielt werden und wie.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="6b7e5-138">Mithilfe von Wiedergabelisten können Sie eine Reihe von Clips definieren, die Schleifen oder wiederholt werden sollen, um die Dauer der Wiedergabe festzulegen und Startzeiten sowie Start-und Endmarker für jeden Eintrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="6b7e5-139">Die Elemente **StartTime**, **Startmarker** und **Endmarker** funktionieren in Verbindung mit Markern in der Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="6b7e5-140">Beispielsweise verwendet die folgende Wiedergabeliste ein Werbebanner und den zugehörigen **moreinfo** -Link in einem **Eintrag** und verweist auf ein **Startmarker** und einen **Endmarker**.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="6b7e5-141">Einstellungs Dauer</span><span class="sxs-lookup"><span data-stu-id="6b7e5-141">Setting Duration</span></span>

<span data-ttu-id="6b7e5-142">Verwenden Sie das **Duration** -Element, um anzugeben, wie lange ein Clip oder eine Reihe von Clips wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="6b7e5-143">Sie können auch das **PreviewMode** -Attribut des **ASX** -Elements in Verbindung mit dem **previewduration** -Element verwenden, um anzugeben, wie lange ein Clip oder eine Reihe von Clips wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="6b7e5-144">Legen Sie das **PreviewMode** -Attribut auf "yes" fest, um mit dem **previewduration** -Element anzugeben, wie lange der zugeordnete Clip wiedergegeben werden soll</span><span class="sxs-lookup"><span data-stu-id="6b7e5-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="6b7e5-145">Die Elemente " **previewduration** " und " **Duration** " weisen das gleiche Verhalten auf.</span><span class="sxs-lookup"><span data-stu-id="6b7e5-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b7e5-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b7e5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7e5-147">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6b7e5-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b7e5-148">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6b7e5-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b7e5-149">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="6b7e5-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6b7e5-150">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="6b7e5-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




