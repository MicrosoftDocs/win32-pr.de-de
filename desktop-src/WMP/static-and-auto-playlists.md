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
# <a name="static-and-auto-playlists"></a>Statische und automatische Wiedergabelisten

Es gibt zwei Arten von Wiedergabelisten:

-   Statische Wiedergabelisten, die bestimmte Medienelemente einschließen
-   Automatische Wiedergabelisten, die die Bibliothek jedes Mal durchsuchen, wenn Sie geöffnet werden, und möglicherweise verschiedene Medienelemente zu unterschiedlichen Zeiten enthalten. Eine automatische Wiedergabeliste ist das Ergebnis einer Datenbankabfrage.

Um eine statische Wiedergabeliste aus einer Metadatei zu importieren, nennen Sie zuerst *Player*. **newwiedergabe** zum Erstellen eines **Wiedergabe** Listen Objekts auf der Grundlage der Daten in der Metadatendatei. übergeben Sie dieses Objekt dann an *playlistcollection*. **importwiedergabe Liste** zum Hinzufügen der Wiedergabeliste zur Bibliothek.

Verwenden Sie zum Importieren einer automatischen Wiedergabeliste aus einer Metadatei *mediacollection*. **fügen Sie hinzu**. Weitere Informationen finden Sie unter [Wiedergabelisten und im mediacollection-Objekt](playlists-and-the-mediacollection-object.md).

Verwenden Sie den *Player*, um eine statische Wiedergabeliste aus einer automatischen Wiedergabelisten-Metadatei zu importieren. **newwiedergabe** und *playlistcollection*. **importplaylist** , wie zuvor beschrieben. Die automatische Wiedergabeliste wird einmal ausgeführt, und basierend auf dem Ergebnis dieser Ausführung wird eine statische Wiedergabeliste erstellt.

Die Verwendung einer automatischen Wiedergabeliste zum Abfragen der Benutzer Bibliothek wird für Webseiten, auf die Benutzer über das Internet zugreifen, nicht unterstützt.

Im folgenden c#-Beispielcode wird das Importieren einer automatischen Wiedergabelisten-Metadatei als statische Wiedergabeliste veranschaulicht. Um dieses Beispiel auszuführen, erstellen Sie mithilfe der Benutzeroberfläche der Bibliothek eine automatische Wiedergabeliste, und fügen Sie dann den richtigen Pfad zur automatischen Wiedergabelisten-Metadatei in diesem Code hinzu.


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

 

 




