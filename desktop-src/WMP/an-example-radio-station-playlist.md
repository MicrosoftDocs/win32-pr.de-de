---
title: Beispiel für eine Radio Station-Wiedergabeliste
description: Beispiel für eine Radio Station-Wiedergabeliste
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Media Metadatei-Wiedergabelisten, Beispiele für Wiedergabelisten
- Wiedergabelisten, Wiedergabelisten Beispiele
- Metadatei-Wiedergabelisten, Wiedergabelisten Beispiele
- Windows Media Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Wiedergabelisten, Beispiel Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Windows Media Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Wiedergabelisten, Beispiel Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Windows Media Metadatei-Wiedergabelisten, Codebeispiel
- Wiedergabelisten, Codebeispiel
- Metadatei-Wiedergabelisten, Codebeispiel
- Windows Media Metadatei-Wiedergabelisten, Beispiel für Radio Station-Wiedergabeliste
- Wiedergabelisten, Beispiel für Radio Stations Wiedergabe
- Metadatendatei-Wiedergabelisten, Beispiel für Radio Stations Wiedergabe
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Beispiel für Windows Media Player, Radio Station-Wiedergabeliste
- Wiedergabelisten Beispiele
- Beispiel Wiedergabelisten
- Beispiel Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388187"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="3a89c-125">Beispiel für eine Radio Station-Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="3a89c-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="3a89c-126">Im folgenden Beispielcode wird veranschaulicht, wie Sie eine Wiedergabeliste erstellen, um drei feldepages zu scannen.</span><span class="sxs-lookup"><span data-stu-id="3a89c-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="3a89c-127">Die fiktive Firma Adventure Works Radio Brand befindet sich in der Wiedergabeliste und in allen einzelnen Streams in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="3a89c-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="3a89c-128">Wenn Sie Ihren Code schreiben, ändern Sie alle URLs und Dateinamen in gültige Dateinamen, die für Ihre Windows-Media Player verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3a89c-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="3a89c-129">Für jede der Stationen wird eine Wiedergabeliste erstellt.</span><span class="sxs-lookup"><span data-stu-id="3a89c-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="3a89c-130">Eine vierte Wiedergabeliste scannt die ersten drei.</span><span class="sxs-lookup"><span data-stu-id="3a89c-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="3a89c-131">Die Wiedergabelisten werden erstellt, um auf dynamisch generierte Ankündigungen zu verweisen und Adventure Works Radio Branding zu haben.</span><span class="sxs-lookup"><span data-stu-id="3a89c-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="3a89c-132">Eine der Wiedergabelisten, die eine Radio Station darstellen, könnte wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="3a89c-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="3a89c-133">Die Wiedergabeliste kann dann aus verweisen auf die einzelnen Wiedergabelisten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a89c-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="3a89c-134">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="3a89c-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="3a89c-135">In diesem Beispiel wird eine Werbe einblenden, gefolgt von 30 Sekunden für jede der drei Stationen, auf die verwiesen wird, abgespielt.</span><span class="sxs-lookup"><span data-stu-id="3a89c-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="3a89c-136">Dieser Cycle wird unbegrenzt wiederholt, da das **count** -Attribut des **Repeat** -Elements nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a89c-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="3a89c-137">Die in den Beispielen verwendeten Firmen, Organisationen, Produkte, Personen und Ereignisse sind frei erfunden, soweit nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3a89c-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="3a89c-138">Jede Ähnlichkeit mit bestehenden Firmen, Organisationen, Produkten, Personen oder Ereignissen ist rein zufällig.</span><span class="sxs-lookup"><span data-stu-id="3a89c-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a89c-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3a89c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a89c-140">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="3a89c-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3a89c-141">**Beispiel Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="3a89c-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="3a89c-142">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="3a89c-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="3a89c-143">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="3a89c-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3a89c-144">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="3a89c-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




