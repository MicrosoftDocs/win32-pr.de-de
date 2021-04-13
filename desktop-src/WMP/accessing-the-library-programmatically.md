---
title: Programm gesteuerter Zugriff auf die Bibliothek
description: Programm gesteuerter Zugriff auf die Bibliothek
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, zugreifen auf Programm gesteuert
- Bibliothek, zugreifen
- Programm gesteuerter Zugriff auf die Windows Media Player-Bibliothek
- Windows Media Player-Bibliothek, Hinzufügen von Medien Elementen
- Bibliothek, Hinzufügen von Medien Elementen
- Windows Media Player-Bibliothek, Abrufen von Medien Elementen
- Bibliothek, Abrufen von Medien Elementen
- Windows Media Player-Bibliothek, Entfernen von Medien Elementen
- Bibliothek, Entfernen von Medien Elementen
- Hinzufügen von Medien Elementen zur Windows-Media Player Bibliothek
- Abrufen von Medien Elementen aus der Windows Media Player-Bibliothek
- Entfernen von Medien Elementen aus der Windows Media Player-Bibliothek
- Abrufen von Metadaten
- Windows Media Player-Bibliothek, Abrufen von Metadaten von Medien Elementen
- Bibliothek, Abrufen von Metadaten von Medien Elementen
- Metadaten, Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388513"
---
# <a name="accessing-the-library-programmatically"></a><span data-ttu-id="48fd6-126">Programm gesteuerter Zugriff auf die Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48fd6-126">Accessing the Library Programmatically</span></span>

<span data-ttu-id="48fd6-127">Im Code wird die Bibliothek durch das **mediacollection** -Objekt (oder die **iwmpmediacollection** -Schnittstelle) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="48fd6-127">In code, the library is represented by the **MediaCollection** object (or the **IWMPMediaCollection** interface).</span></span> <span data-ttu-id="48fd6-128">Medienelemente werden als **Medien** Objekte (oder von der **iwmpmedia** -Schnittstelle) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="48fd6-128">Media items are represented as **Media** objects (or by the **IWMPMedia** interface).</span></span> <span data-ttu-id="48fd6-129">Wiedergabelisten Elemente werden als **Wiedergabe** Listen Objekte dargestellt (oder von der **iwmpwiedergabe** -Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="48fd6-129">Playlist items are represented as **Playlist** objects (or by the **IWMPPlaylist** interface).</span></span> <span data-ttu-id="48fd6-130">Der Einfachheit halber wird in diesem Abschnitt nach Möglichkeit nur auf Objektnamen verwiesen.</span><span class="sxs-lookup"><span data-stu-id="48fd6-130">For simplicity, this section will simply refer to object names, when possible.</span></span>

<span data-ttu-id="48fd6-131">Mithilfe des **mediacollection** -Objekts können Sie mit Medien Elementen und-Wiedergabelisten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="48fd6-131">By using the **MediaCollection** object, you can work with media items and playlists.</span></span> <span data-ttu-id="48fd6-132">Die Bibliothek macht auch das **playlistcollection** -Objekt (oder die **iwmpplaylistcollection** -Schnittstelle) verfügbar, das einige Funktionen bereitstellt, die für die Arbeit mit Wiedergabelisten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="48fd6-132">The library also exposes the **PlaylistCollection** object (or the **IWMPPlaylistCollection** interface), which provides some functionality specific to working with playlists.</span></span> <span data-ttu-id="48fd6-133">In den meisten Fällen stellt das **mediacollection** -Objekt Ihnen die erforderliche Funktionalität zur Verfügung, auch wenn Sie mit Wiedergabelisten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="48fd6-133">Most of the time, the **MediaCollection** object will provide you with the functionality you need, even when working with playlists.</span></span> <span data-ttu-id="48fd6-134">Weitere Informationen zum Arbeiten mit Medien Elementen finden Sie unter [Verwalten von Medien Elementen](managing-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="48fd6-134">For more information about working with media items, see [Managing Media Items](managing-media-items.md).</span></span> <span data-ttu-id="48fd6-135">Weitere Informationen zum Arbeiten mit Wiedergabelisten finden Sie unter [Verwalten von Wiedergabe](managing-playlists.md)Listen.</span><span class="sxs-lookup"><span data-stu-id="48fd6-135">For more information about working with playlists, see [Managing Playlists](managing-playlists.md).</span></span>

## <a name="adding-media-items-to-the-library"></a><span data-ttu-id="48fd6-136">Hinzufügen von Medien Elementen zur Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48fd6-136">Adding Media Items to the Library</span></span>

<span data-ttu-id="48fd6-137">Das Hinzufügen digitaler Medieninhalte zur Bibliothek ist einfach.</span><span class="sxs-lookup"><span data-stu-id="48fd6-137">Adding digital media content to the library is straightforward.</span></span> <span data-ttu-id="48fd6-138">Nennen Sie einfach die [mediacollection. Add](mediacollection-add.md) -Methode, und geben Sie den Pfad zur Mediendatei als Argument an.</span><span class="sxs-lookup"><span data-stu-id="48fd6-138">Simply call the [MediaCollection.add](mediacollection-add.md) method, providing the path to the media file as an argument.</span></span>

## <a name="retrieving-media-items-from-the-library"></a><span data-ttu-id="48fd6-139">Abrufen von Medien Elementen aus der Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48fd6-139">Retrieving Media Items from the Library</span></span>

<span data-ttu-id="48fd6-140">Wenn Sie Medienelemente aus der Bibliothek abrufen, ist das, was Sie wirklich abrufen, eine Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="48fd6-140">When you retrieve media items from the library, what you really retrieve is a playlist.</span></span> <span data-ttu-id="48fd6-141">Auch wenn Sie davon ausgehen, dass nur ein Medien Element abgerufen wird, erhalten Sie ein **Wiedergabe** Listen Objekt, das ein einzelnes Element enthält, das mit dem Index 0 (null) verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="48fd6-141">Even if you expect to retrieve only one media item, you will get a **Playlist** object containing a single item, which will be associated with index zero.</span></span> <span data-ttu-id="48fd6-142">Wenn Sie z. b. ein **Medien** Objekt mit dem Namen "Jeanne" abrufen möchten, können Sie den folgenden JScript-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="48fd6-142">For example, if you want to retrieve a **Media** object that represents the song named "Jeanne", you could use the following JScript code:</span></span>


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



<span data-ttu-id="48fd6-143">Der vorangehende Code Ruft eine Wiedergabeliste ab, die alle Medienelemente mit dem Namen "Jeanne" als Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="48fd6-143">The preceding code retrieves a playlist containing all the media items having the name "Jeanne" as the title.</span></span> <span data-ttu-id="48fd6-144">Nehmen Sie für dieses Beispiel an, dass Sie wissen, dass es in der Bibliothek nur einen Song mit diesem Namen gibt (Beachten Sie, dass die Bibliothek mehrere Lieder mit dem gleichen Namen unterstützt).</span><span class="sxs-lookup"><span data-stu-id="48fd6-144">For this example, assume that you know there is only one song by that name in the library (note that the library supports multiple songs having the same name).</span></span> <span data-ttu-id="48fd6-145">Dies bedeutet, dass Sie erwarten können, dass die Anzahl der Elemente in der Wiedergabeliste, die Sie abgerufen haben, gleich 1 ist, und dass das Medien Element durch Index NULL dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="48fd6-145">This means you could expect the count of items in the playlist you retrieved to equal one and the media item would be represented by index zero.</span></span> <span data-ttu-id="48fd6-146">Im folgenden Beispielcode wird das vorherige Beispiel fortgesetzt, um zu veranschaulichen, wie Sie das Medien Element mithilfe der [Wiedergabe. Item](playlist-item.md) -Methode aus der Wiedergabeliste abrufen.</span><span class="sxs-lookup"><span data-stu-id="48fd6-146">The following example code continues the previous example to demonstrate how you would retrieve the media item from the playlist by using the [Playlist.item](playlist-item.md) method.</span></span>


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



<span data-ttu-id="48fd6-147">Weitere Informationen zum Abrufen von Medien Elementen aus Wiedergabelisten finden Sie unter [Wiedergabelisten und Medienelemente](playlists-and-media-items.md) im [Player-Steuerelement Handbuch](player-control-guide.md).</span><span class="sxs-lookup"><span data-stu-id="48fd6-147">For more information about retrieving media items from playlists, see [Playlists and Media Items](playlists-and-media-items.md) in the [Player Control Guide](player-control-guide.md).</span></span>

## <a name="retrieving-metadata-from-a-media-item"></a><span data-ttu-id="48fd6-148">Abrufen von Metadaten aus einem Medien Element</span><span class="sxs-lookup"><span data-stu-id="48fd6-148">Retrieving Metadata from a Media Item</span></span>

<span data-ttu-id="48fd6-149">Nachdem Sie ein **Medien** Objekt abgerufen haben, können Sie die dem Inhalt zugeordneten Attributwerte lesen.</span><span class="sxs-lookup"><span data-stu-id="48fd6-149">After you retrieve a **Media** object, you can read the attribute values associated with the content.</span></span> <span data-ttu-id="48fd6-150">Im einfachsten Fall möchten Sie vielleicht nur einen einzelnen Wert kennen, z. b. den Namen des Künstlers, der einen Musiktitel durchgeführt hat. Im folgenden JScript-Beispiel wird gezeigt, wie die [Media. getiteminfo](media-getiteminfo.md) -Methode verwendet wird, um den Namen des Künstlers aus den im vorherigen Beispiel abgerufenen Medien abzurufen:</span><span class="sxs-lookup"><span data-stu-id="48fd6-150">In the simplest case, you might simply want to know a single value, such as the name of the artist who performed a music track. The following JScript example shows how to use the [Media.getItemInfo](media-getiteminfo.md) method to retrieve the name of the artist from the media retrieved in the previous example:</span></span>


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



<span data-ttu-id="48fd6-151">Ein Medien Element kann über viele verschiedene Attribute verfügen, und die Arbeit mit Metadaten ist nicht immer so einfach wie die im vorherigen Beispiel gezeigte einfache groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="48fd6-151">A media item can have many different attributes, and working with metadata is not always as straightforward as the simple case shown in the previous example.</span></span> <span data-ttu-id="48fd6-152">Beispielsweise können einige Attribute mehrere Werte enthalten oder Werte in mehr als einer Sprache aufweisen.</span><span class="sxs-lookup"><span data-stu-id="48fd6-152">For instance, some attributes can contain multiple values or have values in more than one language.</span></span> <span data-ttu-id="48fd6-153">Weitere Informationen zum Arbeiten mit Metadaten finden Sie unter [Medien Element Attribute](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="48fd6-153">For more information about working with metadata, see [Media Item Attributes](media-item-attributes.md).</span></span> <span data-ttu-id="48fd6-154">Weitere Informationen zu den verschiedenen Attributen, deren Bedeutungen und Dateityp Unterstützung finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="48fd6-154">For more information about the various attributes, their meanings, and file type support, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="removing-media-items-from-the-library"></a><span data-ttu-id="48fd6-155">Entfernen von Medien Elementen aus der Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48fd6-155">Removing Media Items from the Library</span></span>

<span data-ttu-id="48fd6-156">Das Entfernen digitaler Medieninhalte aus der Bibliothek ist ebenfalls unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="48fd6-156">Removing digital media content from the library is also straightforward.</span></span> <span data-ttu-id="48fd6-157">Nennen Sie einfach " **mediacollection. Remove**", und stellen Sie das **Medien** Objekt, das das Element darstellt, als erstes Argument und den Wert " **true** " als zweiten dar.</span><span class="sxs-lookup"><span data-stu-id="48fd6-157">Simply call **MediaCollection.remove**, providing the **Media** object that represents the item as the first argument and the value **true** as the second.</span></span> <span data-ttu-id="48fd6-158">Im folgenden JScript-Beispiel wird die Datei mit dem Namen "Jeanne (im vorherigen Beispiel abgerufen)" aus der Bibliothek entfernt:</span><span class="sxs-lookup"><span data-stu-id="48fd6-158">The following JScript example removes the file named Jeanne (retrieved in the previous example) from the library:</span></span>


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a><span data-ttu-id="48fd6-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="48fd6-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48fd6-160">**Informationen zur Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="48fd6-160">**About the Library**</span></span>](about-the-library.md)
</dt> <dt>

[<span data-ttu-id="48fd6-161">**Informationen zu mediacollection und Media Objects**</span><span class="sxs-lookup"><span data-stu-id="48fd6-161">**About the MediaCollection and Media Objects**</span></span>](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[<span data-ttu-id="48fd6-162">**Informationen zu den Wiedergabelisten-, playlistcollection-und playlistarray-Objekten**</span><span class="sxs-lookup"><span data-stu-id="48fd6-162">**About the Playlist, PlaylistCollection, and PlaylistArray Objects**</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[<span data-ttu-id="48fd6-163">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="48fd6-163">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




