---
title: Eine einfache Wiedergabeliste
description: Eine einfache Wiedergabeliste
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Windows Media Metadatei-Wiedergabelisten, einfaches Beispiel für Wiedergabeliste
- Wiedergabelisten, einfaches Wiedergabelisten Beispiel
- Metadatei-Wiedergabelisten, einfaches Beispiel für Wiedergabeliste
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Beispiel für Windows Media Player, einfache Wiedergabeliste
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314783"
---
# <a name="a-basic-playlist"></a><span data-ttu-id="10a39-125">Eine einfache Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="10a39-125">A Basic Playlist</span></span>

<span data-ttu-id="10a39-126">Das folgende Wiedergabelisten Beispiel zeigt einen einfachen Satz von Wiedergabelisten Elementen.</span><span class="sxs-lookup"><span data-stu-id="10a39-126">The following playlist example shows a basic set of playlist elements.</span></span> <span data-ttu-id="10a39-127">Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, die für Ihre Windows-Media Player verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="10a39-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="10a39-128">**Code Beispiel**</span><span class="sxs-lookup"><span data-stu-id="10a39-128">**Code Example**</span></span>


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="10a39-129">In der folgenden Tabelle finden Sie ausführliche Informationen zur Verwendung der einzelnen Elemente im Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="10a39-129">The following table provides details on the use of each element in the example code.</span></span>



| <span data-ttu-id="10a39-130">Linie</span><span class="sxs-lookup"><span data-stu-id="10a39-130">Line</span></span>                                                                                            | <span data-ttu-id="10a39-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10a39-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | <span data-ttu-id="10a39-132">Das Element " [ASX](asx-element.md) " identifiziert für den Client (Windows Media Player), dass es sich hierbei um eine Windows Media Metadatei-Wiedergabeliste handelt.</span><span class="sxs-lookup"><span data-stu-id="10a39-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="10a39-133">Das **Versions** Attribut gibt die Versionsnummer der Metadateielemente an.</span><span class="sxs-lookup"><span data-stu-id="10a39-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="10a39-134">\<TITLE>Grundlegende Wiedergabelisten Demo\</TITLE></span><span class="sxs-lookup"><span data-stu-id="10a39-134">\<TITLE>Basic Playlist Demo\</TITLE></span></span>                                                  | <span data-ttu-id="10a39-135">Das [Title](title-element--metafile.md) -Element identifiziert den Titel der Wiedergabeliste als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="10a39-135">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="10a39-136">In Windows Media Player werden diese Metadaten als Show-Titel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="10a39-136">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | <span data-ttu-id="10a39-137">Startet das [Eintrags](entry-element.md) Element.</span><span class="sxs-lookup"><span data-stu-id="10a39-137">Begins the [ENTRY](entry-element.md) element.</span></span> <span data-ttu-id="10a39-138">Ein **Entry** -Element ist eine Möglichkeit, einen bestimmten Clip in einer Wiedergabeliste zu definieren.</span><span class="sxs-lookup"><span data-stu-id="10a39-138">An **ENTRY** element is a way to define a particular clip in a playlist</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="10a39-139">\<TITLE>Ein Eintrag in einer einfachen Wiedergabeliste\</TITLE></span><span class="sxs-lookup"><span data-stu-id="10a39-139">\<TITLE>An Entry in a basic playlist\</TITLE></span></span>                                         | <span data-ttu-id="10a39-140">Gibt den Titel des Wiedergabelisten Clips an.</span><span class="sxs-lookup"><span data-stu-id="10a39-140">Identifies the title of the playlist clip .</span></span> <span data-ttu-id="10a39-141">Sie unterscheidet sich vom vorherigen **Title** -Element, da dieses in einem **Entry** -Element geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="10a39-141">It is different than the previous **TITLE** element because this one is nested within an **ENTRY** element.</span></span> <span data-ttu-id="10a39-142">Windows Media Player zeigt diese Metadaten als Clip Titel an.</span><span class="sxs-lookup"><span data-stu-id="10a39-142">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="10a39-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span><span class="sxs-lookup"><span data-stu-id="10a39-143">\<AUTHOR>Microsoft Corporation\</AUTHOR></span></span>                                              | <span data-ttu-id="10a39-144">Das [Author](author-element.md) -Element identifiziert den Autor des Medienclips.</span><span class="sxs-lookup"><span data-stu-id="10a39-144">The [AUTHOR](author-element.md) element identifies the author of the media clip .</span></span> <span data-ttu-id="10a39-145">Windows Media Player zeigt diese Metadaten als Clip **Autor** an.</span><span class="sxs-lookup"><span data-stu-id="10a39-145">Windows Media Player displays this metadata as the clip **AUTHOR**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | <span data-ttu-id="10a39-146">Kommentar.</span><span class="sxs-lookup"><span data-stu-id="10a39-146">A comment.</span></span> <span data-ttu-id="10a39-147">[Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird, und weisen das gleiche Format wie **XML** -Kommentare auf.</span><span class="sxs-lookup"><span data-stu-id="10a39-147">[Comments](comments.md) are visible only when the code is viewed, and are in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | <span data-ttu-id="10a39-148">Tatsächlicher Zeiger auf die Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="10a39-148">Actual pointer to the media file.</span></span> <span data-ttu-id="10a39-149">Das [ref](ref-element.md) -Element identifiziert die Zeile als Zeiger auf den Medieninhalt, während das **href** -Attribut die URL der Mediendatei ist.</span><span class="sxs-lookup"><span data-stu-id="10a39-149">The [REF](ref-element.md) element identifies the line as a pointer to media content, while the **HREF** attribute is the URL to the media file.</span></span> <span data-ttu-id="10a39-150">In diesem Fall verwendet die URL das MMS-Protokoll, sodass Sie auf einen Windows Media-Server verweist. Mediendateien auf dem Medienserver werden in der Regel nicht am gleichen Speicherort wie Ihre HTML-Dokumente gespeichert.</span><span class="sxs-lookup"><span data-stu-id="10a39-150">In this case, the URL uses the MMS protocol, so it points to a Windows Media server.Media files on your media server are not usually kept in the same location as your HTML documents.</span></span><br/> <span data-ttu-id="10a39-151">Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements "/>" anstelle von " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="10a39-151">Note the use of the XML-like closing of the element , "/>", instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="10a39-152">Da dieses Element nicht über untergeordnete Elemente verfügt, wird es selbst geschlossen.</span><span class="sxs-lookup"><span data-stu-id="10a39-152">Because this element does not have child elements, it closes itself.</span></span><br/> |
| \</ENTRY>                                                                                  | <span data-ttu-id="10a39-153">Gibt das Ende des **Eintrags** Elements an.</span><span class="sxs-lookup"><span data-stu-id="10a39-153">Specifies the end of the **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | <span data-ttu-id="10a39-154">Gibt das Ende der Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="10a39-154">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="10a39-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10a39-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a39-156">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="10a39-156">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="10a39-157">**Beispiel Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="10a39-157">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="10a39-158">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="10a39-158">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="10a39-159">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="10a39-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="10a39-160">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="10a39-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





