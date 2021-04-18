---
title: Wiedergabelisten und das playlistcollection-Objekt
description: Wiedergabelisten und das playlistcollection-Objekt
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, playlistcollection-Objekt
- Metadatei-Wiedergabelisten, playlistcollection-Objekt
- Windows Media Metadatei-Wiedergabelisten, playlistcollection-Objekt
- Playlistcollection-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341225"
---
# <a name="playlists-and-the-playlistcollection-object"></a><span data-ttu-id="ad43f-114">Wiedergabelisten und das playlistcollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="ad43f-114">Playlists and the PlaylistCollection Object</span></span>

<span data-ttu-id="ad43f-115">Das **playlistcollection** -Objekt ermöglicht Ihnen den Zugriff auf Wiedergabelisten in der Bibliothek und verfügt über Methoden zum Erstellen neuer, leerer Wiedergabelisten und neuer Wiedergabelisten aus Metadatendateien.</span><span class="sxs-lookup"><span data-stu-id="ad43f-115">The **PlaylistCollection** object gives you access to playlists in the library and has methods for creating new, empty playlists and new playlists from metafiles.</span></span>

## <a name="working-with-existing-playlists"></a><span data-ttu-id="ad43f-116">Arbeiten mit vorhandenen Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="ad43f-116">Working with Existing Playlists</span></span>

<span data-ttu-id="ad43f-117">Die *playlistcollection*. **GetAll** und *playlistcollection*. die **getByName** -Methoden geben jeweils ein **playlistarray** -Objekt zurück, das mehrere Wiedergabelisten enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="ad43f-117">The *PlaylistCollection*.**getAll** and *PlaylistCollection*.**getByName** methods each return a **PlaylistArray** object, which can contain multiple playlists.</span></span>

<span data-ttu-id="ad43f-118">Die *playlistcollection*. die **GetAll** -Methode gibt alle vorhandenen Wiedergabelisten zurück, die in der Bibliothek vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ad43f-118">The *PlaylistCollection*.**getAll** method returns all of the existing playlists that are in the library.</span></span> <span data-ttu-id="ad43f-119">Beispielsweise können Sie diese Methode aufrufen und dann die Wiedergabelisten im **playlistarray** -Objekt abrufen, um zu bestimmen, ob ein angegebener Wiedergabelisten Name bereits verwendet wurde, oder um alle Wiedergabelisten für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad43f-119">For example, you can call this method and then retrieve the playlists in the **PlaylistArray** object to determine whether a given playlist name has already been used, or to display all of the playlists to the user.</span></span> <span data-ttu-id="ad43f-120">Der Beispielcode in [Wiedergabelisten Attributen](playlist-attributes.md) verwendet die **GetAll** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ad43f-120">The sample code in [Playlist Attributes](playlist-attributes.md) uses the **getAll** method.</span></span>

<span data-ttu-id="ad43f-121">Die *playlistcollection*. die **getByName** -Methode gibt alle Wiedergabelisten mit einem angegebenen Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="ad43f-121">The *PlaylistCollection*.**getByName** method returns all of the playlists with a given name.</span></span> <span data-ttu-id="ad43f-122">Mit dieser Methode können Sie jede dieser Wiedergabelisten separat verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ad43f-122">You can use this method to handle each of those playlists separately.</span></span>

<span data-ttu-id="ad43f-123">Sie können auch die **getByName** -Methode verwenden, um eine eindeutige Wiedergabeliste anhand des Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad43f-123">You can also use the **getByName** method to retrieve a unique playlist by name.</span></span> <span data-ttu-id="ad43f-124">In diesem Fall verfügt das **playlistarray** -Objekt nur über ein Element.</span><span class="sxs-lookup"><span data-stu-id="ad43f-124">In that case, the **PlaylistArray** object has only one element.</span></span> <span data-ttu-id="ad43f-125">Dieses Verfahren wird im folgenden c#-Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ad43f-125">The following C# example demonstrates this technique.</span></span>


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a><span data-ttu-id="ad43f-126">Arbeiten mit neuen Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="ad43f-126">Working with New Playlists</span></span>

<span data-ttu-id="ad43f-127">Sie können den *playlistcollection*-Befehl verwenden. **newwiedergabe** -Methode zum Erstellen einer neuen, leeren Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="ad43f-127">You can use the *PlaylistCollection*.**newPlaylist** method to create a new, empty playlist.</span></span> <span data-ttu-id="ad43f-128">Die-Methode gibt einen Verweis auf das neue **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ad43f-128">The method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="ad43f-129">Sie können dann die *Wiedergabeliste* aufzurufen. **appendItem** -Methode, um der Wiedergabeliste Medienelemente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad43f-129">You can then call the *Playlist*.**appendItem** method to add media items to the playlist.</span></span>

<span data-ttu-id="ad43f-130">Sie können auch eine neue Wiedergabeliste erstellen, die auf einer Wiedergabelisten Metadatei basiert.</span><span class="sxs-lookup"><span data-stu-id="ad43f-130">You can also create a new playlist based on a playlist metafile.</span></span> <span data-ttu-id="ad43f-131">Übergeben Sie zuerst den Namen der Wiedergabeliste und den Pfad an die Metadatendatei an den *Player*. **newwiedergabe** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ad43f-131">First, pass the name of the playlist and the path to the metafile to the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="ad43f-132">Diese Methode gibt einen Verweis auf das neue **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ad43f-132">That method returns a reference to the new **Playlist** object.</span></span> <span data-ttu-id="ad43f-133">Übergeben Sie dann das neue **Wiedergabe** Listen Objekt an die *playlistcollection*. **importwiedergabe** -Methode, um Sie der Bibliothek hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad43f-133">Then, pass the new **Playlist** object to the *PlaylistCollection*.**importPlaylist** method to add it to the library.</span></span>

<span data-ttu-id="ad43f-134">Beachten Sie den Unterschied zwischen *playlistcollection*. **newwiedergabe** -Methode und der *Player*. **newwiedergabe** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ad43f-134">Notice the difference between the *PlaylistCollection*.**newPlaylist** method and the *Player*.**newPlaylist** method.</span></span> <span data-ttu-id="ad43f-135">Die **playlistcollection** -Methode erstellt eine neue, leere Wiedergabeliste und fügt Sie der Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad43f-135">The **PlaylistCollection** method creates a new, empty playlist and adds it to the library.</span></span> <span data-ttu-id="ad43f-136">Die **Player** -Methode erstellt ein neues, aufgefüllte **Wiedergabe** Listen Objekt, fügt es jedoch nicht der Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad43f-136">The **Player** method creates a new, populated **Playlist** object but does not add it to the library.</span></span>

<span data-ttu-id="ad43f-137">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="ad43f-137">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="ad43f-138">Im folgenden c#-Beispiel wird das Importieren einer Wiedergabeliste aus einer Metadatei veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ad43f-138">The following C# example demonstrates importing a playlist from a metafile.</span></span> <span data-ttu-id="ad43f-139">Das " *strinplistname* "-Argument gibt den Namen der neuen Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="ad43f-139">The *strPListName* argument specifies the name of the new playlist.</span></span> <span data-ttu-id="ad43f-140">Der " *strinmetafilename* " gibt den Namen der Metadatendatei an, aus der die Wiedergabeliste importiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad43f-140">The *strMetaFileName* specifies the name of the metafile from which the playlist is imported.</span></span>


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a><span data-ttu-id="ad43f-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad43f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad43f-142">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="ad43f-142">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="ad43f-143">**Player. newwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="ad43f-143">**Player.newPlaylist**</span></span>](player-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="ad43f-144">**Wiedergabeliste. appendItem**</span><span class="sxs-lookup"><span data-stu-id="ad43f-144">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="ad43f-145">**Playlistarray-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ad43f-145">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="ad43f-146">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ad43f-146">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ad43f-147">**Wiedergabelisten und Medienelemente**</span><span class="sxs-lookup"><span data-stu-id="ad43f-147">**Playlists and Media Items**</span></span>](playlists-and-media-items.md)
</dt> </dl>

 

 




