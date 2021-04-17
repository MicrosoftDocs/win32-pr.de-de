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
# <a name="playlists-and-the-mediacollection-object"></a>Wiedergabelisten und das mediacollection-Objekt

Das **mediacollection** -Objekt ermöglicht Ihnen den Zugriff auf eine Vielzahl von speziellen Wiedergabelisten und umfasst eine Methode zum Erstellen einer neuen Wiedergabeliste aus einer Metadatei.

Die folgenden Methoden rufen besondere Wiedergabelisten ab:

-   **"GetAll"**
-   **getbyalbum**
-   **getbyattribute**
-   **getbyauthor**
-   **getByGenre**
-   **getByName**

Wie ihre Namen vermuten, rufen diese Methoden Wiedergabelisten ab, die alle Medienelemente in der Bibliothek enthalten, die bestimmten Kriterien entsprechen.

Achten Sie darauf, die *mediacollection* nicht zu verwechseln. **getByName** -Methode mit *playlistcollection*. **getByName** -Methode. Die **mediacollection** -Methode gibt ein **Wiedergabe** Listen Objekt zurück, das alle Medienelemente mit dem angegebenen Namen enthält. Die **playlistcollection** -Methode gibt ein **playlistarray** -Objekt zurück, das alle Wiedergabelisten mit dem angegebenen Namen enthält.

Sie können das *mediacollection*-Ereignis verwenden. **fügen Sie** eine Methode hinzu, um Wiedergabelisten und Medienelemente der Bibliothek hinzuzufügen. Zum Hinzufügen einer Wiedergabeliste übergeben Sie der-Methode den Pfad an die Metadatendatei, die die Wiedergabeliste definiert. Die-Methode gibt immer ein **Medien** Objekt zurück. Zwischen **Medien** -und **Wiedergabe** Listen Objekten kann nicht umgewandelt werden. Wenn Sie mit der Wiedergabeliste arbeiten möchten, die Sie hinzugefügt haben, rufen Sie das **Wiedergabe** Listen Objekt ab, das denselben Namen wie das **Medien** Objekt aufweist.

Im folgenden c#-Beispiel wird veranschaulicht, wie Medien mithilfe von **mediacollection** nach Typ abgerufen werden. **getbyattribute** -Methode. Dieser Code Ruft die Namen aller Attribute ab, die einem bestimmten Typ zugeordnet sind, sowie den Lese-/Schreib-oder schreibgeschützten Status dieser Attribute. Es wird eine einzelne Datei generiert, die Listen mit Attributen für die Typen Audiodaten, Video, Radio, Wiedergabeliste, andere, Musik und Foto enthält.


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



Im folgenden c#-Beispiel wird veranschaulicht, wie der Bibliothek eine Wiedergabeliste aus einer Metadatei hinzugefügt wird.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Statische Wiedergabelisten enthalten bestimmte Medienelemente. Automatische Wiedergabelisten durchsuchen die Bibliothek jedes Mal, wenn Sie geöffnet werden, und können zu unterschiedlichen Zeitpunkten unterschiedliche Medienelemente enthalten. Sie können der Bibliothek mithilfe von *mediacollection* sowohl statische als auch automatische Wiedergabelisten hinzufügen. Methode **Hinzufügen** . Sie können statische Wiedergabelisten auch mithilfe von *playlistcollection* hinzufügen. **importwiedergabe** -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Wiedergabelisten und das playlistcollection-Objekt**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Statische und automatische Wiedergabelisten**](static-and-auto-playlists.md)
</dt> </dl>

 

 




