---
title: Wiedergabelisten und das MediaCollection-Objekt
description: Wiedergabelisten und das MediaCollection-Objekt
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player,Wiedergabelisten
- Windows Media Player-Objektmodell,Wiedergabelisten
- Objektmodell,Wiedergabelisten
- Windows Media Player Mobil, Wiedergabelisten
- Windows Media Player ActiveX,Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement,Wiedergabelisten
- ActiveX,Wiedergabelisten
- playlists,MediaCollection-Objekt
- Metafile-Wiedergabelisten, MediaCollection-Objekt
- Windows Medienmetadatei-Wiedergabelisten,MediaCollection-Objekt
- MediaCollection-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a0bba2e966e51523dc24965c2f2a066767b059f26a08fde9ee5856a1694df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334453"
---
# <a name="playlists-and-the-mediacollection-object"></a>Wiedergabelisten und das MediaCollection-Objekt

Das **MediaCollection-Objekt** bietet Ihnen Zugriff auf eine Vielzahl von speziellen Wiedergabelisten und enthält eine Methode zum Erstellen einer neuen Wiedergabeliste aus einer Metadatei.

Die folgenden Methoden rufen spezielle Wiedergabelisten ab:

-   **getAll**
-   **getBy Instanz**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Wie ihre Namen vermuten lassen, rufen diese Methoden Wiedergabelisten ab, die alle Medienelemente in der Bibliothek enthalten, die bestimmte Kriterien erfüllen.

Achten Sie darauf, die *MediaCollection nicht zu verwechseln.* **getByName-Methode** mit der *PlaylistCollection.* **getByName-Methode.** Die **MediaCollection-Methode** gibt ein **Playlist-Objekt** zurück, das alle Medienelemente mit dem angegebenen Namen enthält. Die **PlaylistCollection-Methode** gibt ein **PlaylistArray-Objekt** zurück, das alle Wiedergabelisten mit dem angegebenen Namen enthält.

Sie können *mediaCollection verwenden.* **Fügen Sie** die -Methode hinzu, um Wiedergabelisten sowie Medienelemente zur Bibliothek hinzuzufügen. Um eine Wiedergabeliste hinzuzufügen, übergeben Sie der -Methode den Pfad zur Metadatei, die die Wiedergabeliste definiert. Die -Methode gibt immer ein **Media-Objekt** zurück. Sie können nicht zwischen **Medien- und** **Wiedergabelistenobjekten** umstellen. Um mit der wiedergabeliste zu arbeiten, die Sie hinzugefügt haben, rufen Sie das **Playlist-Objekt** ab, das den gleichen Namen wie das **Medienobjekt** hat.

Im folgenden C#-Beispiel wird veranschaulicht, wie Medien mithilfe von MediaCollection nach Typ **abgerufen werden.** **getByAttribute-Methode.** Dieser Code ruft die Namen aller Attribute ab, die einem bestimmten Typ zugeordnet sind, sowie den Lese-/Schreibstatus oder den schreibgeschützten Status dieser Attribute. Es wird eine einzelne Datei generiert, die Listen mit Attributen für die Typen Audio, Video, Radio, Playlist, Other, Musik und Photo enthält.


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



Im folgenden C#-Beispiel wird veranschaulicht, wie der Bibliothek eine Wiedergabeliste aus einer Metadatei hinzugefügt wird.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Statische Wiedergabelisten enthalten bestimmte Medienelemente. Automatische Wiedergabelisten durchsuchen die Bibliothek jedes Mal, wenn sie geöffnet werden, und enthalten möglicherweise zu unterschiedlichen Zeiten unterschiedliche Medienelemente. Sie können der Bibliothek sowohl statische als auch automatische Wiedergabelisten hinzufügen, indem Sie *mediaCollection verwenden.* **add-Methode.** Sie können statische Wiedergabelisten auch mithilfe der *PlaylistCollection hinzufügen.* **importPlaylist-Methode.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Wiedergabelisten und das PlaylistCollection-Objekt**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Statische und automatische Wiedergabelisten**](static-and-auto-playlists.md)
</dt> </dl>

 

 




