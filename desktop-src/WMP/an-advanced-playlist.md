---
title: Eine erweiterte Wiedergabeliste
description: Eine erweiterte Wiedergabeliste
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Windows Media Metadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel für erweiterte Wiedergabelisten
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036752"
---
# <a name="an-advanced-playlist"></a><span data-ttu-id="96a23-125">Eine erweiterte Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="96a23-125">An Advanced Playlist</span></span>

<span data-ttu-id="96a23-126">Im folgenden Wiedergabelisten Beispiel wird gezeigt, wie ein ausführlichere Satz von Wiedergabelisten Elementen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96a23-126">The following playlist example shows how to use a more complete set of playlist elements.</span></span> <span data-ttu-id="96a23-127">Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, die für Ihre Windows-Media Player verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="96a23-127">When writing your own code, you will need to change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="96a23-128">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="96a23-128">Example Code</span></span>


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="96a23-129">In der folgenden Tabelle wird die vorangehende erweiterte Wiedergabeliste beschrieben.</span><span class="sxs-lookup"><span data-stu-id="96a23-129">The following table describes the preceding advanced playlist.</span></span>



| <span data-ttu-id="96a23-130">Zeile</span><span class="sxs-lookup"><span data-stu-id="96a23-130">Line</span></span>                                                                                            | <span data-ttu-id="96a23-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96a23-131">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | <span data-ttu-id="96a23-132">Das Element " [ASX](asx-element.md) " identifiziert für den Client (Windows Media Player), dass es sich hierbei um eine Windows Media Metadatei-Wiedergabeliste handelt.</span><span class="sxs-lookup"><span data-stu-id="96a23-132">The [ASX](asx-element.md) element identifies for the client (Windows Media Player) that this is a Windows Media metafile playlist.</span></span> <span data-ttu-id="96a23-133">Das **Versions** Attribut gibt die Versionsnummer der Metadateielemente an.</span><span class="sxs-lookup"><span data-stu-id="96a23-133">The **version** attribute specifies the version number of the metafile elements.</span></span>                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | <span data-ttu-id="96a23-134">Das [Title](title-element--metafile.md) -Element identifiziert den Titel der Wiedergabeliste als Ganzes.</span><span class="sxs-lookup"><span data-stu-id="96a23-134">The [TITLE](title-element--metafile.md) element identifies the title of the playlist as a whole.</span></span> <span data-ttu-id="96a23-135">In Windows Media Player werden diese Metadaten als Show-Titel angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96a23-135">Windows Media Player displays this metadata as the show title.</span></span>                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | <span data-ttu-id="96a23-136">Das [abstrakte](abstract-element.md) Element stellt die QuickInfo für den Show-Titel bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-136">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the show title.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | <span data-ttu-id="96a23-137">Das [moreinfo](moreinfo-element.md) -Element verknüpft den Show-Titel mit einer URL.</span><span class="sxs-lookup"><span data-stu-id="96a23-137">The [MOREINFO](moreinfo-element.md) element links the show title to an URL.</span></span> <span data-ttu-id="96a23-138">Wenn Sie den Mauszeiger über den Show-Titel bewegen, greift auf die QuickInfo zu, falls definiert.</span><span class="sxs-lookup"><span data-stu-id="96a23-138">Pausing the mouse pointer over the show title accesses the ToolTip, if defined.</span></span> <span data-ttu-id="96a23-139">Wenn Sie den Titel anzeigen auswählen, wird die festgelegte URL geöffnet.</span><span class="sxs-lookup"><span data-stu-id="96a23-139">Selecting the show title will then open the designated URL.</span></span>                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | <span data-ttu-id="96a23-140">Das [Banner](banner-element.md) -Element erstellt ein Werbe Banner in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="96a23-140">The [BANNER](banner-element.md) element creates an advertising banner in Windows Media Player.</span></span> <span data-ttu-id="96a23-141">Das **href** -Attribut gibt die Banner Grafik an (die 194 Pixel breit und 32 Pixel hoch sein muss).</span><span class="sxs-lookup"><span data-stu-id="96a23-141">The **HREF** attribute specifies the banner graphic (which must be 194 pixels wide by 32 pixels tall).</span></span>                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | <span data-ttu-id="96a23-142">Das [abstrakte](abstract-element.md) Element stellt die QuickInfo für das **Banner** bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-142">The [ABSTRACT](abstract-element.md) element provides the ToolTip for the **BANNER**.</span></span>                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | <span data-ttu-id="96a23-143">Das [Moran FO](moreinfo-element.md) -Element verknüpft die **Banner** Grafik mit einer URL.</span><span class="sxs-lookup"><span data-stu-id="96a23-143">The [MOREINFO](moreinfo-element.md) element links the **BANNER** graphic to a URL.</span></span> <span data-ttu-id="96a23-144">Wenn Sie mit dem Mauszeiger auf das **Banner** zugreifen, wird eine QuickInfo angezeigt, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="96a23-144">Holding the mouse pointer over the **BANNER** accesses a ToolTip, if defined.</span></span> <span data-ttu-id="96a23-145">Wenn Sie das **Banner** auswählen, wird die festgelegte URL geöffnet.</span><span class="sxs-lookup"><span data-stu-id="96a23-145">Selecting the **BANNER** will open the designated URL.</span></span>                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | <span data-ttu-id="96a23-146">Das [param](param-element.md) -Element definiert einen benutzerdefinierten Parameter.</span><span class="sxs-lookup"><span data-stu-id="96a23-146">The [PARAM](param-element.md) element defines a custom parameter.</span></span> <span data-ttu-id="96a23-147">Mit dem **Name** -Attribut wird der Name des benutzerdefinierten Parameters als "Track" definiert.</span><span class="sxs-lookup"><span data-stu-id="96a23-147">The **name** attribute defines the name of the custom parameter as "track".</span></span> <span data-ttu-id="96a23-148">Das **value** -Attribut definiert den Wert von "Track" als "1".</span><span class="sxs-lookup"><span data-stu-id="96a23-148">The **value** attribute defines the value of "track" to be "1".</span></span>                                                                                                                          |
| `</BANNER>`                                                                                 | <span data-ttu-id="96a23-149">Schließt das **Banner** Element.</span><span class="sxs-lookup"><span data-stu-id="96a23-149">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | <span data-ttu-id="96a23-150">Beginnt den Block " [Entry](entry-element.md) Element".</span><span class="sxs-lookup"><span data-stu-id="96a23-150">Begins the [ENTRY](entry-element.md) element block.</span></span> <span data-ttu-id="96a23-151">Dieses Element definiert einen Clip in einer Wiedergabeliste durch Angeben eines Links im **ref** -Element.</span><span class="sxs-lookup"><span data-stu-id="96a23-151">This element defines a clip in a playlist by specifying a link in the **REF** element.</span></span> <span data-ttu-id="96a23-152">Wenn **clientskip** auf "No" festgelegt wird, kann der Benutzer nicht schnell vorwärts wechseln oder zum nächsten Clip springen.</span><span class="sxs-lookup"><span data-stu-id="96a23-152">Setting **ClientSkip** to "no" means that the user cannot fast forward or jump to the next clip</span></span>                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | <span data-ttu-id="96a23-153">Erstellt ein Werbebanner.</span><span class="sxs-lookup"><span data-stu-id="96a23-153">Creates an advertising banner.</span></span> <span data-ttu-id="96a23-154">Der **href** ist die Banner Grafik (194x32 Pixel).</span><span class="sxs-lookup"><span data-stu-id="96a23-154">The **HREF** is the banner graphic (194x32 pixels).</span></span>                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | <span data-ttu-id="96a23-155">Stellt die QuickInfo für das Banner bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-155">Provides the ToolTip for the banner.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="96a23-156">Stellt einen Link zur URL für das Banner bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-156">Provides a link to the URL for the banner.</span></span> <span data-ttu-id="96a23-157">Die Auswahl des Banners stellt eine Verbindung mit der URL her.</span><span class="sxs-lookup"><span data-stu-id="96a23-157">Selecting the banner connects to the URL.</span></span>                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | <span data-ttu-id="96a23-158">Schließt das **Banner** Element.</span><span class="sxs-lookup"><span data-stu-id="96a23-158">Closes the **BANNER** element</span></span>                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | <span data-ttu-id="96a23-159">Stellt einen Link zur URL für den Clip **Titel** Text bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-159">Provides a link to the URL for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | <span data-ttu-id="96a23-160">Kommentar.</span><span class="sxs-lookup"><span data-stu-id="96a23-160">A comment.</span></span> <span data-ttu-id="96a23-161">[Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96a23-161">[Comments](comments.md) are only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | <span data-ttu-id="96a23-162">Stellt die QuickInfo für den Clip **Titel** Text bereit.</span><span class="sxs-lookup"><span data-stu-id="96a23-162">Provides the ToolTip for the clip **Title** text.</span></span>                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | <span data-ttu-id="96a23-163">Gibt den Titel des Clips an.</span><span class="sxs-lookup"><span data-stu-id="96a23-163">Identifies the title of the clip.</span></span> <span data-ttu-id="96a23-164">Dies ist der Clip- **Titel** , da er in einem **Entry** -Element geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="96a23-164">It is the clip **TITLE** because it is nested within an **ENTRY** element.</span></span> <span data-ttu-id="96a23-165">Windows Media Player zeigt diese Metadaten als Clip Titel an.</span><span class="sxs-lookup"><span data-stu-id="96a23-165">Windows Media Player displays this metadata as the clip title.</span></span>                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | <span data-ttu-id="96a23-166">Identifiziert den Autor des Medienclips.</span><span class="sxs-lookup"><span data-stu-id="96a23-166">Identifies the author of the media clip.</span></span> <span data-ttu-id="96a23-167">Diese Metadaten werden als Clip- **Autor** von Windows Media Player angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96a23-167">This metadata is displayed as the clip **AUTHOR** by Windows Media Player.</span></span>                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | <span data-ttu-id="96a23-168">Das [Copyright](copyright-element.md) -Element gibt die dem Medien Clip zugeordneten Urheberrechte an.</span><span class="sxs-lookup"><span data-stu-id="96a23-168">The [COPYRIGHT](copyright-element.md) element specifies the copyrights associated with the media clip.</span></span> <span data-ttu-id="96a23-169">In Windows Media Player werden diese Metadaten als Clip Copyright angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96a23-169">Windows Media Player displays this metadata as the clip COPYRIGHT.</span></span>                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="96a23-170">Ein Kommentar im gleichen Format wie **XML** -Kommentare.</span><span class="sxs-lookup"><span data-stu-id="96a23-170">A comment, in the same format as **XML** comments.</span></span>                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | <span data-ttu-id="96a23-171">Die URL für den Medieninhalt.</span><span class="sxs-lookup"><span data-stu-id="96a23-171">URL for the media content.</span></span> <span data-ttu-id="96a23-172">Das [ref](ref-element.md) -Element identifiziert die Zeile als Zeiger auf den Medieninhalt.</span><span class="sxs-lookup"><span data-stu-id="96a23-172">The [REF](ref-element.md) element identifies the line as a pointer to media content.</span></span> <span data-ttu-id="96a23-173">Das **href** -Attribut ist die URL der Datei. Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements "/>" anstelle von " &lt; /ref &gt; ".</span><span class="sxs-lookup"><span data-stu-id="96a23-173">The **HREF** attribute is the URL to the file.Note the use of the XML-like closing of the element , "/>" instead of "&lt;/REF&gt;".</span></span> <span data-ttu-id="96a23-174">Da dieses Element nicht über untergeordnete Elemente verfügt, wird es selbst geschlossen.</span><span class="sxs-lookup"><span data-stu-id="96a23-174">Because this element does not have child elements, it closes itself.</span></span><br/> |
| `</ENTRY>`                                                                                  | <span data-ttu-id="96a23-175">Gibt das Ende der des ersten **Entry** -Elements an.</span><span class="sxs-lookup"><span data-stu-id="96a23-175">Specifies the end of the of the first **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | <span data-ttu-id="96a23-176">Startet das zweite **Entry** -Element.</span><span class="sxs-lookup"><span data-stu-id="96a23-176">Begins the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | <span data-ttu-id="96a23-177">Gibt den Titel des zweiten Clips an.</span><span class="sxs-lookup"><span data-stu-id="96a23-177">Identifies the title of the second clip.</span></span>                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | <span data-ttu-id="96a23-178">Identifiziert den Autor des zweiten Medienclips.</span><span class="sxs-lookup"><span data-stu-id="96a23-178">Identifies the author of the second media clip.</span></span>                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | <span data-ttu-id="96a23-179">Kommentar.</span><span class="sxs-lookup"><span data-stu-id="96a23-179">A comment.</span></span> <span data-ttu-id="96a23-180">Er ist nur sichtbar, wenn der Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96a23-180">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | <span data-ttu-id="96a23-181">Dies ist der QuickInfo-Text für den **Titeltext** des Clips.</span><span class="sxs-lookup"><span data-stu-id="96a23-181">This is the ToolTip text for the **TITLE** text of the clip.</span></span>                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | <span data-ttu-id="96a23-182">Kommentar.</span><span class="sxs-lookup"><span data-stu-id="96a23-182">A comment.</span></span> <span data-ttu-id="96a23-183">Er ist nur sichtbar, wenn der Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96a23-183">It will only be visible when the code is viewed.</span></span>                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | <span data-ttu-id="96a23-184">Identifiziert die Zeile als Zeiger auf Medieninhalt.</span><span class="sxs-lookup"><span data-stu-id="96a23-184">Identifies the line as a pointer to media content.</span></span> <span data-ttu-id="96a23-185">Das **href** -Attribut ist die URL der Datei.</span><span class="sxs-lookup"><span data-stu-id="96a23-185">The **HREF** attribute is the URL to the file.</span></span>                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | <span data-ttu-id="96a23-186">Gibt das Ende des zweiten **Entry** -Elements an.</span><span class="sxs-lookup"><span data-stu-id="96a23-186">Specifies the end of the second **ENTRY** element.</span></span>                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | <span data-ttu-id="96a23-187">Gibt das Ende der Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="96a23-187">Specifies the end of the playlist.</span></span>                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="96a23-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96a23-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a23-189">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="96a23-189">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="96a23-190">**Beispiel Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="96a23-190">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="96a23-191">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="96a23-191">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="96a23-192">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="96a23-192">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="96a23-193">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="96a23-193">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 





