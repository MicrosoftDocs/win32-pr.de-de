---
title: Statische und automatische Wiedergabelisten
description: Statische und automatische Wiedergabelisten
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, statisch
- Metadatei-Wiedergabelisten, statisch
- Windows Media Metadatei-Wiedergabelisten, statisch
- statische Wiedergabelisten
- automatische Wiedergabelisten
- Wiedergabelisten, automatisch
- Metadatei-Wiedergabelisten, automatisch
- Windows Media Metadatei-Wiedergabelisten, automatisch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388054"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="427bc-118">Statische und automatische Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="427bc-118">Static and Auto Playlists</span></span>

<span data-ttu-id="427bc-119">Es gibt zwei Arten von Wiedergabelisten:</span><span class="sxs-lookup"><span data-stu-id="427bc-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="427bc-120">Statische Wiedergabelisten, die bestimmte Medienelemente einschließen</span><span class="sxs-lookup"><span data-stu-id="427bc-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="427bc-121">Automatische Wiedergabelisten, die die Bibliothek jedes Mal durchsuchen, wenn Sie geöffnet werden, und möglicherweise verschiedene Medienelemente zu unterschiedlichen Zeiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="427bc-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="427bc-122">Eine automatische Wiedergabeliste ist das Ergebnis einer Datenbankabfrage.</span><span class="sxs-lookup"><span data-stu-id="427bc-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="427bc-123">Um eine statische Wiedergabeliste aus einer Metadatei zu importieren, nennen Sie zuerst *Player*. **newwiedergabe** zum Erstellen eines **Wiedergabe** Listen Objekts auf der Grundlage der Daten in der Metadatendatei. übergeben Sie dieses Objekt dann an *playlistcollection*. **importwiedergabe Liste** zum Hinzufügen der Wiedergabeliste zur Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="427bc-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="427bc-124">Verwenden Sie zum Importieren einer automatischen Wiedergabeliste aus einer Metadatei *mediacollection*. **fügen Sie hinzu**.</span><span class="sxs-lookup"><span data-stu-id="427bc-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="427bc-125">Weitere Informationen finden Sie unter [Wiedergabelisten und im mediacollection-Objekt](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="427bc-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="427bc-126">Verwenden Sie den *Player*, um eine statische Wiedergabeliste aus einer automatischen Wiedergabelisten-Metadatei zu importieren. **newwiedergabe** und *playlistcollection*. **importplaylist** , wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="427bc-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="427bc-127">Die automatische Wiedergabeliste wird einmal ausgeführt, und basierend auf dem Ergebnis dieser Ausführung wird eine statische Wiedergabeliste erstellt.</span><span class="sxs-lookup"><span data-stu-id="427bc-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="427bc-128">Die Verwendung einer automatischen Wiedergabeliste zum Abfragen der Benutzer Bibliothek wird für Webseiten, auf die Benutzer über das Internet zugreifen, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="427bc-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="427bc-129">Im folgenden c#-Beispielcode wird das Importieren einer automatischen Wiedergabelisten-Metadatei als statische Wiedergabeliste veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="427bc-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="427bc-130">Um dieses Beispiel auszuführen, erstellen Sie mithilfe der Benutzeroberfläche der Bibliothek eine automatische Wiedergabeliste, und fügen Sie dann den richtigen Pfad zur automatischen Wiedergabelisten-Metadatei in diesem Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="427bc-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="427bc-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="427bc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427bc-132">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="427bc-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




