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
# <a name="playlists-and-the-playlistcollection-object"></a>Wiedergabelisten und das playlistcollection-Objekt

Das **playlistcollection** -Objekt ermöglicht Ihnen den Zugriff auf Wiedergabelisten in der Bibliothek und verfügt über Methoden zum Erstellen neuer, leerer Wiedergabelisten und neuer Wiedergabelisten aus Metadatendateien.

## <a name="working-with-existing-playlists"></a>Arbeiten mit vorhandenen Wiedergabelisten

Die *playlistcollection*. **GetAll** und *playlistcollection*. die **getByName** -Methoden geben jeweils ein **playlistarray** -Objekt zurück, das mehrere Wiedergabelisten enthalten kann.

Die *playlistcollection*. die **GetAll** -Methode gibt alle vorhandenen Wiedergabelisten zurück, die in der Bibliothek vorhanden sind. Beispielsweise können Sie diese Methode aufrufen und dann die Wiedergabelisten im **playlistarray** -Objekt abrufen, um zu bestimmen, ob ein angegebener Wiedergabelisten Name bereits verwendet wurde, oder um alle Wiedergabelisten für den Benutzer anzuzeigen. Der Beispielcode in [Wiedergabelisten Attributen](playlist-attributes.md) verwendet die **GetAll** -Methode.

Die *playlistcollection*. die **getByName** -Methode gibt alle Wiedergabelisten mit einem angegebenen Namen zurück. Mit dieser Methode können Sie jede dieser Wiedergabelisten separat verarbeiten.

Sie können auch die **getByName** -Methode verwenden, um eine eindeutige Wiedergabeliste anhand des Namens abzurufen. In diesem Fall verfügt das **playlistarray** -Objekt nur über ein Element. Dieses Verfahren wird im folgenden c#-Beispiel veranschaulicht.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Arbeiten mit neuen Wiedergabelisten

Sie können den *playlistcollection*-Befehl verwenden. **newwiedergabe** -Methode zum Erstellen einer neuen, leeren Wiedergabeliste. Die-Methode gibt einen Verweis auf das neue **Wiedergabe** Listen Objekt zurück. Sie können dann die *Wiedergabeliste* aufzurufen. **appendItem** -Methode, um der Wiedergabeliste Medienelemente hinzuzufügen.

Sie können auch eine neue Wiedergabeliste erstellen, die auf einer Wiedergabelisten Metadatei basiert. Übergeben Sie zuerst den Namen der Wiedergabeliste und den Pfad an die Metadatendatei an den *Player*. **newwiedergabe** -Methode. Diese Methode gibt einen Verweis auf das neue **Wiedergabe** Listen Objekt zurück. Übergeben Sie dann das neue **Wiedergabe** Listen Objekt an die *playlistcollection*. **importwiedergabe** -Methode, um Sie der Bibliothek hinzuzufügen.

Beachten Sie den Unterschied zwischen *playlistcollection*. **newwiedergabe** -Methode und der *Player*. **newwiedergabe** -Methode. Die **playlistcollection** -Methode erstellt eine neue, leere Wiedergabeliste und fügt Sie der Bibliothek hinzu. Die **Player** -Methode erstellt ein neues, aufgefüllte **Wiedergabe** Listen Objekt, fügt es jedoch nicht der Bibliothek hinzu.

In diesem Thema wurde das **Player** -Objekt wie folgt definiert:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



Im folgenden c#-Beispiel wird das Importieren einer Wiedergabeliste aus einer Metadatei veranschaulicht. Das " *strinplistname* "-Argument gibt den Namen der neuen Wiedergabeliste an. Der " *strinmetafilename* " gibt den Namen der Metadatendatei an, aus der die Wiedergabeliste importiert wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Player. newwiedergabe**](player-newplaylist.md)
</dt> <dt>

[**Wiedergabeliste. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlistarray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Wiedergabelisten und Medienelemente**](playlists-and-media-items.md)
</dt> </dl>

 

 




