---
title: Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten
description: Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, Wiedergabelisten Objekt
- Windows Media Player-Objektmodell, Wiedergabelisten Objekt
- Objektmodell, Wiedergabelisten Objekt
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten Objekt
- ActiveX-Steuerelement, Wiedergabelisten Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten Objekt
- Windows Media Player Mobile, Wiedergabelisten Objekt
- Wiedergabelisten Objekt
- Windows Media Player, playlistcollection-Objekt
- Windows Media Player-Objektmodell, playlistcollection-Objekt
- Objektmodell, playlistcollection-Objekt
- Windows Media Player ActiveX-Steuerelement, playlistcollection-Objekt
- ActiveX-Steuerelement, playlistcollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, playlistcollection-Objekt
- Windows Media Player Mobile, playlistcollection-Objekt
- Playlistcollection-Objekt
- Windows Media Player, playlistarray-Objekt
- Windows Media Player-Objektmodell, playlistarray-Objekt
- Object Model, playlistarray-Objekt
- Windows Media Player ActiveX-Steuerelement, playlistarray-Objekt
- ActiveX-Steuerelement, playlistarray-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, playlistarray-Objekt
- Windows Media Player Mobile, playlistarray-Objekt
- Playlistarray-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337572"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a><span data-ttu-id="5f1b6-127">Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten</span><span class="sxs-lookup"><span data-stu-id="5f1b6-127">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>

<span data-ttu-id="5f1b6-128">Die **Wiedergabe** Listen, **playlistcollection** und **playlistarray** -Objekte steuern die Wiedergabelisten, die von Windows Media Player verwendet werden können, um die Reihenfolge anzugeben, in der der Inhalt wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-128">The **Playlist**, **PlaylistCollection**, and **PlaylistArray** objects govern the playlists that Windows Media Player can use to specify the order in which content will be played.</span></span> <span data-ttu-id="5f1b6-129">Sie erhalten das **playlistcollection** -Objekt aus der **playlistcollection** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-129">You get the **PlaylistCollection** object from the **playlistCollection** property of the **Player** object.</span></span> <span data-ttu-id="5f1b6-130">Die **playlistcollection** -Eigenschaft gibt das **playlistcollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-130">The **playlistCollection** property returns the **PlaylistCollection** object.</span></span> <span data-ttu-id="5f1b6-131">Sie können nur auf die Eigenschaften des **playlistcollection** -Objekts zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-131">You can only access the properties of the **PlaylistCollection** object after you have created it.</span></span> <span data-ttu-id="5f1b6-132">Wenn Sie z. b. eine neue Wiedergabeliste erstellen möchten, müssen Sie zuerst das **playlistcollection** -Objekt und dann eine-Methode für dieses Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-132">For example, to create a new playlist, you must first get the **PlaylistCollection** object and then use a method on that object.</span></span>


```C++
player.playlistcollection.newplaylist('myplaylist');
```



<span data-ttu-id="5f1b6-133">Sie können die aktuelle Wiedergabeliste mit der **currentwiedergabe** -Eigenschaft erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-133">You can get the current playlist by using the **currentPlaylist** property.</span></span> <span data-ttu-id="5f1b6-134">Um z. b. den Namen der aktuellen Wiedergabeliste zu erhalten, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="5f1b6-134">For example, to get the name of the current playlist, use the following code:</span></span>


```C++
myname = player.currentplaylist.name;
```



<span data-ttu-id="5f1b6-135">Das **playlistarray** -Objekt wird von den Methoden **GetAll** und **getByName** des **playlistcollection** -Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f1b6-135">The **PlaylistArray** object is returned by the **getAll** and **getByName** methods of the **PlaylistCollection** object.</span></span> <span data-ttu-id="5f1b6-136">Um beispielsweise die Anzahl der Wiedergabelisten zu erhalten, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="5f1b6-136">To get the number of playlists, for example, use the following code:</span></span>


```C++
howmany = player.playlistcollection.getAll().count;
```



<span data-ttu-id="5f1b6-137">Verwenden Sie den folgenden Code, um eine bekannte Wiedergabeliste nach Namen abzurufen:</span><span class="sxs-lookup"><span data-stu-id="5f1b6-137">To retrieve a known playlist by name, use the following code:</span></span>


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="5f1b6-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f1b6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f1b6-139">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="5f1b6-139">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="5f1b6-140">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="5f1b6-140">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5f1b6-141">**Playlistarray-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5f1b6-141">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="5f1b6-142">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5f1b6-142">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 




