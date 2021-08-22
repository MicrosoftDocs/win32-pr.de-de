---
title: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
description: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Onlineshops, automatische Wiedergabelisten
- Onlineshops, automatische Wiedergabelisten
- Geben Sie 1 Onlineshops ein, automatische Wiedergabelisten
- Geben Sie 2 Onlineshops ein, automatische Wiedergabelisten.
- Windows Media Player Onlineshops, Organisieren von Bibliotheksinhalten
- Onlineshops, Organisieren von Bibliotheksinhalten
- Typ 1 Onlineshops, Organisieren von Bibliotheksinhalten
- Typ 2 Onlineshops, Organisieren von Bibliotheksinhalten
- Windows Media Player Onlineshops, Organisieren von Bibliotheksinhalten
- Onlineshops, Organisieren von Bibliotheksinhalten
- Typ 1 Onlineshops, Organisieren von Bibliotheksinhalten
- Typ 2 Onlineshops, Organisieren von Bibliotheksinhalten
- Bibliothek,Organisieren von Inhalten
- Organisieren von Bibliotheksinhalten
- Automatische Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e32d0f95093d9550c71643330267d59a57f56db7e0d666274a492ac29b2c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507170"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek

Sie können automatische Wiedergabelisten verwenden, um die von Ihnen zur Verfügung stellen Premium-Inhalte zu organisieren. Beispielsweise können Sie Windows Media Player verwenden, um eine automatische Wiedergabeliste zu erstellen, die nur inhalte enthält, die Sie mit einer Benutzerbewertung von mindestens vier Sternen bereitgestellt haben. Anschließend können Sie die automatische Wiedergabeliste der Bibliothek in Windows Media Player hinzufügen, sodass sie im Knoten Erworbene Musik unter dem Knoten Ihres Inhaltsverteilers angezeigt wird.

Gehen Sie hierzu folgendermaßen vor:

1.  Erstellen Sie die automatische Wiedergabeliste.
2.  Navigieren Sie mit Windows Explorer zur automatischen Wiedergabeliste, und rufen Sie die WPL-Datei ab.
3.  Fügen Sie die automatische Wiedergabeliste mithilfe des Windows Media Player-Objektmodells der Bibliothek hinzu.
4.  Legen Sie das **WM/ContentDistributor-Attribut** für die Wiedergabeliste auf den Schlüsselnamen Ihres Inhaltsverteilers fest.
5.  Legen Sie das **SyncOnly-Attribut** für die Wiedergabeliste auf TRUE fest.

Der folgende JScript Beispielcode zeigt eine Funktion, die dem Proseware-Knoten in der Bibliothek eine automatische Wiedergabeliste namens "Favoritentreffer" hinzufügt:


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Bibliotheksintegration](download-manager-overview.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und Typ 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Statische und automatische Wiedergabelisten**](static-and-auto-playlists.md)
</dt> <dt>

[**SyncOnly-Attribut**](synconly-attribute.md)
</dt> <dt>

[**WM/ContentDistributor-Attribut**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




