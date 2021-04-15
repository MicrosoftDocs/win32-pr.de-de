---
title: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
description: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online Stores, automatische Wiedergabelisten
- Online Stores, automatische Wiedergabelisten
- Typ 1 Online Stores, automatische Wiedergabelisten
- Typ 2 Online Stores, automatische Wiedergabelisten
- Windows Media Player Online Stores, organisieren von Bibliotheks Inhalten
- Online Stores, organisieren von Bibliotheks Inhalten
- Geben Sie 1 Online Stores ein, organisieren Sie Bibliotheksinhalte.
- Typ 2 Online Stores, organisieren von Bibliotheksinhalt
- Windows Media Player Online Stores, organisieren von Bibliotheks Inhalten
- Online Stores, organisieren von Bibliotheks Inhalten
- Typ 1 Online Stores, Bibliothek Inhalt organisieren
- Typ 2 Online Stores, Bibliothek Inhalt organisieren
- Bibliothek, organisieren von Inhalten
- Organisieren von Bibliotheksinhalt
- automatische Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515866"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek

Sie können automatische Wiedergabelisten verwenden, um von Ihnen bereitgestellte Premium-Inhalte zu organisieren. Beispielsweise können Sie mit Windows Media Player eine automatische Wiedergabeliste erstellen, die nur Inhalte enthält, die Sie mit einer Benutzer Bewertung von mindestens vier Sternen angegeben haben. Anschließend können Sie die automatische Wiedergabeliste der Bibliothek in Windows Media Player hinzufügen, sodass Sie im Knoten "erworbene Musik" unter Ihrem Inhalts Verteilerknoten angezeigt wird.

Gehen Sie hierzu folgendermaßen vor:

1.  Erstellen Sie die automatische Wiedergabeliste.
2.  Navigieren Sie in Windows-Explorer zur automatischen Wiedergabeliste, und rufen Sie die WPL-Datei ab.
3.  Fügen Sie der Bibliothek mithilfe des Windows Media Player-Objektmodells die automatische Wiedergabeliste hinzu.
4.  Legen Sie das **WM/contentdistributor-** Attribut für die Wiedergabeliste auf den Schlüsselnamen ihres Inhalts Verteilers fest.
5.  Legen Sie das **synattribute** -Attribut für die Wiedergabeliste auf true fest.

Der folgende JScript-Beispielcode zeigt eine Funktion, die dem Proseware-Knoten in der Bibliothek eine automatische Wiedergabeliste mit dem Namen "Favoriten Treffer" hinzufügt:


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

[Informationen zur Bibliotheks Integration](download-manager-overview.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Wiedergabeliste. Einstellungs Element**](playlist-setiteminfo.md)
</dt> <dt>

[**Statische und automatische Wiedergabelisten**](static-and-auto-playlists.md)
</dt> <dt>

[**Synkonstante-Attribut**](synconly-attribute.md)
</dt> <dt>

[**WM-/contentverteilungs-Attribut**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




