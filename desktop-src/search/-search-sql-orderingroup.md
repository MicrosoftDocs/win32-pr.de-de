---
description: Die ORDER IN GROUP-Klausel wird in Verbindung mit der GROUP ON-Anweisung verwendet, die Result Sets in Gruppen zurückgibt.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: ORDER IN GROUP-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17981f6368b67852e393d38ef8c4b856601d73014d9bdce40292e7e4a499d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944650"
---
# <a name="order-in-group-clause"></a>ORDER IN GROUP-Klausel

Die ORDER IN GROUP-Klausel wird in Verbindung mit der [GROUP ON-Anweisung](-search-sql-group-on-over.md) verwendet, die Result Sets in Gruppen zurückgibt. Mit der ORDER IN GROUP-Klausel können Sie jede zurückgegebene Gruppe auf andere Weise sortieren. Wenn Sie beispielsweise nach System.Kind gruppen, können Sie alle Dokumente nach System.Docsortieren. LastAuthor, alle Musikdateien nach System. Musik. AlbumArtist und alle E-Mails von System.Message.FromName.

## <a name="syntax"></a>Syntax

Im Folgenden finden Sie die Syntax der ORDER IN GROUP-Klausel:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



Der Gruppennamenspezifizierer ist ein Bereich oder ein bekannter Wert aus der Gruppenspalte, wie in der GROUP ON-Anweisung angegeben. Zu den bekannten Werten für System.Photo.ISOSpeed zählen beispielsweise "ISO-100", "ISO-200" und so weiter. Ein Bereich für System.Photo.DateTaken würde "2006-1-1" und "2007-1-1" für eine Anweisung wie GROUP ON System.ItemDate \[ '2006-1-1', '2007-1-1' \] enthalten.

Der Spaltenspezifizierer muss eine gültige Spalte sein, die in der GROUP ON- oder SELECT-Anweisung angegeben ist. Sie können mehrere Spalten durch Kommas getrennt hinzufügen. Wenn Sie beispielsweise nach System.Photo.ISOSpeed gruppieren, können Sie alle ISO-100-Fotos sortieren, zuerst nach System.Photo.SpeedSpeed und dann nach System.Photo.Aperture.

Der optionale Richtungsspezifizierer kann entweder ASC für aufsteigend (niedrig bis hoch) oder DESC für absteigend (hoch bis niedrig) sein. Wenn Sie keinen Richtungsspezifizierer bereitstellen, wird der Standardwert (aufsteigend) verwendet. Wenn Sie mehr als eine Spalte angeben, aber nicht alle Richtungen angeben, wird die Richtung, die Sie zuletzt angeben, auf jede nachfolgende Spalte angewendet, bis Sie die Richtung explizit ändern.

Bereiche oder Werte, die nicht explizit in einer ORDER GROUP IN-Klausel angegeben sind, werden in aufsteigender Reihenfolge nach den Werten in der GROUP ON-Spalte sortiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden Die Ergebnisse nach der System.Kind-Eigenschaft gegruppen. Die Abfrage ordnet die Gruppe "Program" nach dem Anwendungsnamen und die Gruppe "music" nach Titel und Titelnummer des Albums an. Die **NULL-Gruppe** wird nach dem Elementnamen geordnet. Alle anderen Gruppen werden nach dem Elementdatum geordnet.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



Im folgenden Beispiel werden die Ergebnisse nach der System.ItemDate-Eigenschaft und dann jede Gruppe nach Element-URL, Art oder Name sortiert.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Die Ergebnisse der vorherigen Abfrage werden in fünf Gruppen zurückgegeben und wie in der folgenden Tabelle beschrieben sortiert.



| Gruppieren    | Beschreibung                                               | Sortiert nach:                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| Minvalue | Elemente mit Datumsangaben vor 2006-1-1                          | Sortiert nach der URL des Elements in aufsteigender Reihenfolge |
| 2006-1-1 | Elemente mit Datumsangaben am oder nach 2006-1-1, aber vor 2007-1-1 | Sortiert nach Elementdatum in aufsteigender Reihenfolge      |
| 2007-1-1 | Elemente mit Datumsangaben am oder nach 2007-1-1, aber vor 2008-1-1 | Sortiert nach Artwert in aufsteigender Reihenfolge     |
| 2008-1-1 | Elemente mit Datumsangaben am oder nach dem 1.1.2008                     | Sortiert nach Elementdatum in aufsteigender Reihenfolge      |
| **NULL** | Elemente ohne Wert in der Spalte System.ItemDate         | Sortiert nach Elementname in aufsteigender Reihenfolge      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[GROUP ON ... Über... Anweisung](-search-sql-group-on-over.md)
</dt> <dt>

[ORDER BY-Klausel](-search-sql-orderby.md)
</dt> </dl>

 

 



