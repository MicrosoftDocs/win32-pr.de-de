---
title: Programmgesteuerter Zugriff auf die Bibliothek
description: Programmgesteuerter Zugriff auf die Bibliothek
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player,Library
- Windows Media Player-Objektmodell,Bibliothek
- Objektmodell,Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobil, Bibliothek für Objektmodell
- Windows Media Player Bibliothek,Programmgesteuerter Zugriff
- Bibliothek,Zugreifen auf
- Programmgesteuertes Zugreifen auf Windows Media Player Bibliothek
- Windows Media Player Bibliothek, Hinzufügen von Medienelementen
- Bibliothek, Hinzufügen von Medienelementen
- Windows Media Player Bibliothek,Abrufen von Medienelementen
- Bibliothek,Abrufen von Medienelementen
- Windows Media Player Bibliothek,Entfernen von Medienelementen
- Bibliothek,Entfernen von Medienelementen
- Hinzufügen von Medienelementen zu Windows Media Player Bibliothek
- Abrufen von Medienelementen aus Windows Media Player Bibliothek
- Entfernen von Medienelementen aus Windows Media Player Bibliothek
- Abrufen von Metadaten
- Windows Media Player Bibliothek,Abrufen von Metadaten aus Medienelementen
- Bibliothek, Abrufen von Metadaten aus Medienelementen
- Metadaten,Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d1ed265d5c8e65beab9cc8e937b3639d8547867dacf473b2db21fe99198
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619430"
---
# <a name="accessing-the-library-programmatically"></a>Programmgesteuerter Zugriff auf die Bibliothek

Im Code wird die Bibliothek durch das **MediaCollection-Objekt** (oder die **IWMPMediaCollection-Schnittstelle)** dargestellt. Medienelemente werden als **Medienobjekte** (oder durch die **IWMPMedia-Schnittstelle)** dargestellt. Wiedergabelistenelemente werden als **Wiedergabelistenobjekte** (oder durch die **IWMPPlaylist-Schnittstelle)** dargestellt. Der Einfachheit halber wird in diesem Abschnitt nach Möglichkeit einfach auf Objektnamen verwiesen.

Mithilfe des **MediaCollection-Objekts** können Sie mit Medienelementen und Wiedergabelisten arbeiten. Die Bibliothek macht auch das **PlaylistCollection-Objekt** (oder die **IWMPPlaylistCollection-Schnittstelle)** verfügbar, das bestimmte Funktionen für die Arbeit mit Wiedergabelisten bereitstellt. In den meisten Jahren stellt das **MediaCollection-Objekt** Ihnen die funktionalität bereit, die Sie benötigen, auch wenn Sie mit Wiedergabelisten arbeiten. Weitere Informationen zum Arbeiten mit Medienelementen finden Sie unter [Verwalten von Medienelementen.](managing-media-items.md) Weitere Informationen zum Arbeiten mit Wiedergabelisten finden Sie unter [Verwalten von Wiedergabelisten.](managing-playlists.md)

## <a name="adding-media-items-to-the-library"></a>Hinzufügen von Medienelementen zur Bibliothek

Das Hinzufügen digitaler Medieninhalte zur Bibliothek ist einfach. Rufen Sie einfach die [MediaCollection.add-Methode](mediacollection-add.md) auf, und geben Sie den Pfad zur Mediendatei als Argument an.

## <a name="retrieving-media-items-from-the-library"></a>Abrufen von Medienelementen aus der Bibliothek

Wenn Sie Medienelemente aus der Bibliothek abrufen, ist das, was Sie wirklich abrufen, eine Wiedergabeliste. Auch wenn Sie nur ein Medienelement abrufen möchten, erhalten Sie ein **Wiedergabelistenobjekt,** das ein einzelnes Element enthält, das index 0 (null) zugeordnet wird. Wenn Sie z. B. ein **Media-Objekt** abrufen möchten, das den Titel "Sender" darstellt, können Sie den folgenden JScript Code verwenden:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



Der vorangehende Code ruft eine Wiedergabeliste ab, die alle Medienelemente mit dem Namen "Soll" als Titel enthält. Nehmen Sie für dieses Beispiel an, dass sie wissen, dass nur ein Titel mit diesem Namen in der Bibliothek vorhanden ist (beachten Sie, dass die Bibliothek mehrere Titel mit demselben Namen unterstützt). Dies bedeutet, dass Sie erwarten könnten, dass die Anzahl der Elemente in der abgerufenen Wiedergabeliste gleich 1 ist und das Medienelement durch index 0 (null) dargestellt wird. Der folgende Beispielcode setzt das vorherige Beispiel fort, um zu veranschaulichen, wie Sie das Medienelement mithilfe der [Playlist.item-Methode](playlist-item.md) aus der Wiedergabeliste abrufen würden.


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Weitere Informationen zum Abrufen von Medienelementen aus Wiedergabelisten finden Sie unter [Wiedergabelisten und Medienelemente](playlists-and-media-items.md) im [Player-Steuerelementhandbuch.](player-control-guide.md)

## <a name="retrieving-metadata-from-a-media-item"></a>Abrufen von Metadaten aus einem Medienelement

Nachdem Sie ein **Media-Objekt** abgerufen haben, können Sie die Attributwerte lesen, die dem Inhalt zugeordnet sind. Im einfachsten Fall möchten Sie vielleicht einfach einen einzelnen Wert kennen, z. B. den Namen des Interpreten, der einen Musiktitel ausgeführt hat. Im folgenden JScript Beispiel wird gezeigt, wie Sie die [Media.getItemInfo-Methode](media-getiteminfo.md) verwenden, um den Namen des Interpreten von den Medien abzurufen, die im vorherigen Beispiel abgerufen wurden:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Ein Medienelement kann viele verschiedene Attribute aufweisen, und das Arbeiten mit Metadaten ist nicht immer so einfach wie der im vorherigen Beispiel gezeigte einfache Fall. Einige Attribute können z. B. mehrere Werte oder Werte in mehreren Sprachen enthalten. Weitere Informationen zum Arbeiten mit Metadaten finden Sie unter [Media Item Attributes](media-item-attributes.md). Weitere Informationen zu den verschiedenen Attributen, deren Bedeutungen und zur Unterstützung von Dateitypen finden Sie in der [Attributreferenz](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Entfernen von Medienelementen aus der Bibliothek

Das Entfernen digitaler Medieninhalte aus der Bibliothek ist ebenfalls einfach. Rufen Sie einfach **MediaCollection.remove** auf, und geben Sie das **Media-Objekt** an, das das Element als erstes Argument und den Wert **TRUE** als zweites darstellt. Im folgenden JScript Beispiel wird die Datei namens Heißt (im vorherigen Beispiel abgerufen) aus der Bibliothek entfernt:


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Bibliothek**](about-the-library.md)
</dt> <dt>

[**Informationen zu MediaCollection und Medienobjekten**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Informationen zu den Objekten "Playlist", "PlaylistCollection" und "PlaylistArray"**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




