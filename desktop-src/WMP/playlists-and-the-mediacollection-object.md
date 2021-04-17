---
title: Wiedergabelisten und das mediacollection-Objekt
description: Wiedergabelisten und das mediacollection-Objekt
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, mediacollection-Objekt
- Metadatei-Wiedergabelisten, mediacollection-Objekt
- Windows Media Metadatei-Wiedergabelisten, mediacollection-Objekt
- Mediacollection-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388148"
---
# <a name="playlists-and-the-mediacollection-object"></a><span data-ttu-id="245fb-114">Wiedergabelisten und das mediacollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="245fb-114">Playlists and the MediaCollection Object</span></span>

<span data-ttu-id="245fb-115">Das **mediacollection** -Objekt ermöglicht Ihnen den Zugriff auf eine Vielzahl von speziellen Wiedergabelisten und umfasst eine Methode zum Erstellen einer neuen Wiedergabeliste aus einer Metadatei.</span><span class="sxs-lookup"><span data-stu-id="245fb-115">The **MediaCollection** object gives you access to a variety of special playlists, and includes a method for creating a new playlist from a metafile.</span></span>

<span data-ttu-id="245fb-116">Die folgenden Methoden rufen besondere Wiedergabelisten ab:</span><span class="sxs-lookup"><span data-stu-id="245fb-116">The following methods retrieve special playlists:</span></span>

-   <span data-ttu-id="245fb-117">**"GetAll"**</span><span class="sxs-lookup"><span data-stu-id="245fb-117">**getAll**</span></span>
-   <span data-ttu-id="245fb-118">**getbyalbum**</span><span class="sxs-lookup"><span data-stu-id="245fb-118">**getByAlbum**</span></span>
-   <span data-ttu-id="245fb-119">**getbyattribute**</span><span class="sxs-lookup"><span data-stu-id="245fb-119">**getByAttribute**</span></span>
-   <span data-ttu-id="245fb-120">**getbyauthor**</span><span class="sxs-lookup"><span data-stu-id="245fb-120">**getByAuthor**</span></span>
-   <span data-ttu-id="245fb-121">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="245fb-121">**getByGenre**</span></span>
-   <span data-ttu-id="245fb-122">**getByName**</span><span class="sxs-lookup"><span data-stu-id="245fb-122">**getByName**</span></span>

<span data-ttu-id="245fb-123">Wie ihre Namen vermuten, rufen diese Methoden Wiedergabelisten ab, die alle Medienelemente in der Bibliothek enthalten, die bestimmten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="245fb-123">As their names suggest, these methods retrieve playlists containing all of the media items in the library that match certain criteria.</span></span>

<span data-ttu-id="245fb-124">Achten Sie darauf, die *mediacollection* nicht zu verwechseln. **getByName** -Methode mit *playlistcollection*. **getByName** -Methode.</span><span class="sxs-lookup"><span data-stu-id="245fb-124">Be careful not to confuse the *MediaCollection*.**getByName** method with the *PlaylistCollection*.**getByName** method.</span></span> <span data-ttu-id="245fb-125">Die **mediacollection** -Methode gibt ein **Wiedergabe** Listen Objekt zurück, das alle Medienelemente mit dem angegebenen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="245fb-125">The **MediaCollection** method returns a **Playlist** object containing all of the media items that have the specified name.</span></span> <span data-ttu-id="245fb-126">Die **playlistcollection** -Methode gibt ein **playlistarray** -Objekt zurück, das alle Wiedergabelisten mit dem angegebenen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="245fb-126">The **PlaylistCollection** method returns a **PlaylistArray** object containing all of the playlists that have the specified name.</span></span>

<span data-ttu-id="245fb-127">Sie können das *mediacollection*-Ereignis verwenden. **fügen Sie** eine Methode hinzu, um Wiedergabelisten und Medienelemente der Bibliothek hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="245fb-127">You can use the *MediaCollection*.**add** method to add playlists as well as media items to the library.</span></span> <span data-ttu-id="245fb-128">Zum Hinzufügen einer Wiedergabeliste übergeben Sie der-Methode den Pfad an die Metadatendatei, die die Wiedergabeliste definiert.</span><span class="sxs-lookup"><span data-stu-id="245fb-128">To add a playlist, you pass the method the path to the metafile that defines the playlist.</span></span> <span data-ttu-id="245fb-129">Die-Methode gibt immer ein **Medien** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="245fb-129">The method always returns a **Media** object.</span></span> <span data-ttu-id="245fb-130">Zwischen **Medien** -und **Wiedergabe** Listen Objekten kann nicht umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="245fb-130">You cannot cast between **Media** and **Playlist** objects.</span></span> <span data-ttu-id="245fb-131">Wenn Sie mit der Wiedergabeliste arbeiten möchten, die Sie hinzugefügt haben, rufen Sie das **Wiedergabe** Listen Objekt ab, das denselben Namen wie das **Medien** Objekt aufweist.</span><span class="sxs-lookup"><span data-stu-id="245fb-131">To work with the playlist that you added, retrieve the **Playlist** object that has the same name as the **Media** object.</span></span>

<span data-ttu-id="245fb-132">Im folgenden c#-Beispiel wird veranschaulicht, wie Medien mithilfe von **mediacollection** nach Typ abgerufen werden. **getbyattribute** -Methode.</span><span class="sxs-lookup"><span data-stu-id="245fb-132">The following C# example demonstrates how to retrieve media by type using the **MediaCollection**.**getByAttribute** method.</span></span> <span data-ttu-id="245fb-133">Dieser Code Ruft die Namen aller Attribute ab, die einem bestimmten Typ zugeordnet sind, sowie den Lese-/Schreib-oder schreibgeschützten Status dieser Attribute.</span><span class="sxs-lookup"><span data-stu-id="245fb-133">This code retrieves the names of all attributes associated with a given type as well as the read/write or read-only status of those attributes.</span></span> <span data-ttu-id="245fb-134">Es wird eine einzelne Datei generiert, die Listen mit Attributen für die Typen Audiodaten, Video, Radio, Wiedergabeliste, andere, Musik und Foto enthält.</span><span class="sxs-lookup"><span data-stu-id="245fb-134">It generates a single file that contains lists of attributes for the Audio, Video, Radio, Playlist, Other, Music, and Photo types.</span></span>


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



<span data-ttu-id="245fb-135">Im folgenden c#-Beispiel wird veranschaulicht, wie der Bibliothek eine Wiedergabeliste aus einer Metadatei hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="245fb-135">The following C# example demonstrates how to add a playlist from a metafile to the library.</span></span>


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



<span data-ttu-id="245fb-136">Statische Wiedergabelisten enthalten bestimmte Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="245fb-136">Static playlists include specific media items.</span></span> <span data-ttu-id="245fb-137">Automatische Wiedergabelisten durchsuchen die Bibliothek jedes Mal, wenn Sie geöffnet werden, und können zu unterschiedlichen Zeitpunkten unterschiedliche Medienelemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="245fb-137">Auto playlists search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="245fb-138">Sie können der Bibliothek mithilfe von *mediacollection* sowohl statische als auch automatische Wiedergabelisten hinzufügen. Methode **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="245fb-138">You can add both static and auto playlists to the library by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="245fb-139">Sie können statische Wiedergabelisten auch mithilfe von *playlistcollection* hinzufügen. **importwiedergabe** -Methode.</span><span class="sxs-lookup"><span data-stu-id="245fb-139">You can also add static playlists by using the *PlaylistCollection*.**importPlaylist** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="245fb-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="245fb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="245fb-141">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="245fb-141">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="245fb-142">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="245fb-142">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="245fb-143">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="245fb-143">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="245fb-144">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="245fb-144">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="245fb-145">**Wiedergabelisten und das playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="245fb-145">**Playlists and the PlaylistCollection Object**</span></span>](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="245fb-146">**Statische und automatische Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="245fb-146">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> </dl>

 

 




