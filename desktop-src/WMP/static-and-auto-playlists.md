---
title: Statische und automatische Wiedergabelisten
description: Statische und automatische Wiedergabelisten
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player,Wiedergabelisten
- Windows Media Player-Objektmodell,Wiedergabelisten
- Objektmodell,Wiedergabelisten
- Windows Media Player Mobil, Wiedergabelisten
- Windows Media Player ActiveX,Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement,Wiedergabelisten
- ActiveX,Wiedergabelisten
- Wiedergabelisten,statisch
- Metafile-Wiedergabelisten, statisch
- Windows Wiedergabelisten von Medienmetadateien, statisch
- Statische Wiedergabelisten
- Automatische Wiedergabelisten
- Wiedergabelisten,auto
- Metafile-Wiedergabelisten,auto
- Windows Wiedergabelisten von Medienmetadateien,auto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645b3bd9ca9ddeebcce9fd6cbb905caa54717e87876be6e449ebd4d3ab64a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568782"
---
# <a name="static-and-auto-playlists"></a>Statische und automatische Wiedergabelisten

Es gibt zwei Arten von Wiedergabelisten:

-   Statische Wiedergabelisten, die bestimmte Medienelemente enthalten
-   Automatische Wiedergabelisten, die die Bibliothek jedes Mal durchsuchen, wenn sie geöffnet werden und zu unterschiedlichen Zeiten unterschiedliche Medienelemente enthalten können. Eine automatische Wiedergabeliste ist das Ergebnis einer Datenbankabfrage.

Um eine statische Wiedergabeliste aus einer Metadatei zu importieren, rufen Sie zuerst *Player auf.* **newPlaylist,** um ein **Playlist-Objekt** basierend auf den Daten in der Metadatei zu erstellen und dieses Objekt dann an *PlaylistCollection zu übergeben.* **importPlaylist zum** Hinzufügen der Wiedergabeliste zur Bibliothek.

Verwenden Sie MediaCollection, um eine automatische Wiedergabeliste aus einer *Metadatei zu importieren.* **fügen Sie hinzu.** Weitere Informationen finden Sie unter [Wiedergabelisten und das MediaCollection-Objekt.](playlists-and-the-mediacollection-object.md)

Verwenden Sie Player , um eine statische Wiedergabeliste aus einer Metadatei für die automatische *Wiedergabeliste zu importieren.* **newPlaylist** und *PlaylistCollection*. **importPlaylist wie** zuvor beschrieben. Die automatische Wiedergabeliste wird einmal ausgeführt, und basierend auf dem Ergebnis dieser Ausführung wird eine statische Wiedergabeliste erstellt.

Die Verwendung einer automatischen Wiedergabeliste zum Abfragen der Benutzerbibliothek wird für Webseiten, auf die Benutzer über das Internet zugreifen, nicht unterstützt.

Der folgende C#-Beispielcode veranschaulicht das Importieren einer Metadatei für die automatische Wiedergabeliste als statische Wiedergabeliste. Erstellen Sie zum Ausführen dieses Beispiels mithilfe der Bibliotheksoberfläche eine automatische Wiedergabeliste, und fügen Sie dann den richtigen Pfad zur Metadatei für die automatische Wiedergabeliste in diesen Code ein.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwalten von Wiedergabelisten**](managing-playlists.md)
</dt> </dl>

 

 




