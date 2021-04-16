---
description: Die Order in Group-Klausel wird in Verbindung mit der Group on-Anweisung verwendet, die Resultsets in Gruppen zurückgibt.
ms.assetid: edfa2037-3360-411d-8a12-cdb9680222f2
title: Order in Group-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b4a3a39ffeb2704a099389a6668a075fb4a24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342949"
---
# <a name="order-in-group-clause"></a>Order in Group-Klausel

Die Order in Group-Klausel wird in Verbindung mit der [Group on](-search-sql-group-on-over.md) -Anweisung verwendet, die Resultsets in Gruppen zurückgibt. Mit der Order in Group-Klausel können Sie jede zurückgegebene Gruppe auf andere Weise sortieren. Wenn Sie z. b. nach System. Kind gruppieren, können Sie alle Dokumente nach System.Doc-Nummer sortieren. Lastauthor, alle Musikdateien nach System. Music. albumartist und alle e-Mails nach System. Message. FromName.

## <a name="syntax"></a>Syntax

Im folgenden finden Sie die Syntax der Order in Group-Klausel:


```
GROUP ON <group column and optional ranges>
OVER (SELECT ... FROM SystemIndex
    ORDER 
        IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]]
        [IN GROUP '<group name>' BY <column> [<direction>] [,<column> [<direction>]] ]
        [BY <column> [<direction>] [,<column> [<direction>]] ])
```



Der gruppennamensspezifizierer ist ein Bereich oder ein bekannter Wert aus der Gruppenspalte, wie in der Group on-Anweisung angegeben. Zu den bekannten Werten für System. Photo. Isospeed zählen z. b. "ISO-100", "ISO-200" usw. Ein Bereich für System. Photo. DateTaken würde "2006-1-1" und "2007-1-1" für eine Anweisung wie "Group" in System. itemdate \[ "2006-1-1", "2007-1-1" enthalten \] .

Der Spalten Spezifizierer muss eine gültige Spalte sein, die entweder in der Gruppe on oder der SELECT-Anweisung angegeben ist. Sie können mehr als eine Spalte einschließen, getrennt durch Kommas. Wenn Sie z. b. System. Photo. Isospeed gruppieren, können Sie alle ISO-100-Fotos zuerst nach "System. Photo. shutterspeed" und dann nach "System. Photo. Aperture" sortieren.

Der optionale richtungsspezifizierer kann entweder ASC für aufsteigend (niedrig zu hoch) oder für absteigend (hoch bis niedrig) sein. Wenn Sie keinen richtungsspezifizierer angeben, wird der Standardwert aufsteigend verwendet. Wenn Sie mehr als eine Spalte angeben, aber nicht alle Richtungen angeben, wird die von Ihnen angegebene Richtung zuletzt auf jede aufeinander folgende Spalte angewendet, bis Sie die Richtung explizit ändern.

Bereiche oder Werte, die nicht explizit in einer Order Group in-Klausel angegeben sind, werden in aufsteigender Reihenfolge nach den Werten in der Spalte Gruppieren nach sortiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden die Ergebnisse nach der System. Kind-Eigenschaft gruppiert. Die Abfrage würde die Gruppe "Program" nach dem Namen der Anwendung und der Gruppe "Music" nach Albumtitel und Nachverfolgen der Nummer sortieren. Die **null** -Gruppe wird nach dem Elementnamen geordnet. Alle anderen Gruppen würden nach dem Element Datum geordnet.


```
GROUP ON System.Kind 
OVER (SELECT System.ItemUrl, System.Music.AlbumTitle, System.Music.TrackNumber, System.ItemName, System.ItemDate, System.Kind FROM SystemIndex
    ORDER 
        IN GROUP 'program' BY System.ApplicationName ASC
        IN GROUP 'music' BY System.Music.AlbumTitle ASC, System.Music.TrackNumber ASC
        IN GROUP NULL BY System.ItemName
        BY System.ItemDate DESC)
```



Im folgenden Beispiel werden die Ergebnisse nach der System. itemdate-Eigenschaft gruppiert. Anschließend werden die einzelnen Gruppen nach Element-URL, Art oder Name sortiert.


```
GROUP ON System.ItemDate ['2006-1-1', '2007-1-1', '2008-1-1'] 
OVER (SELECT System.ItemUrl, System.ItemName, System.ItemDate System.Kind FROM SystemIndex
    ORDER 
        IN GROUP MINVALUE BY System.ItemUrl ASC
        IN GROUP '2007-1-1' BY System.Kind
        IN GROUP NULL BY System.ItemName)
```



Die Ergebnisse der vorhergehenden Abfrage werden in fünf Gruppen zurückgegeben und entsprechend der Beschreibung in der folgenden Tabelle sortiert.



| Gruppieren    | Beschreibung                                               | Sortiert nach:                                    |
|----------|-----------------------------------------------------------|----------------------------------------------|
| MinValue | Elemente mit Datumsangaben vor 2006-1-1                          | Sortiert nach der Element-URL in aufsteigender Reihenfolge |
| 2006-1-1 | Elemente mit Datumsangaben auf oder nach 2006-1-1, aber vor 2007-1-1 | Sortiert nach Element Datum in aufsteigender Reihenfolge      |
| 2007-1-1 | Elemente mit Datumsangaben auf oder nach 2007-1-1, aber vor 2008-1-1 | Sortiert nach Kind-Wert in aufsteigender Reihenfolge     |
| 2008-1-1 | Elemente mit Datumsangaben auf oder nach 2008-1-1                     | Sortiert nach Element Datum in aufsteigender Reihenfolge      |
| **NULL** | Elemente ohne Wert in der System. itemdate-Spalte         | Sortiert nach Elementname in aufsteigender Reihenfolge      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Gruppieren nach... Über... An](-search-sql-group-on-over.md)
</dt> <dt>

[Order By-Klausel](-search-sql-orderby.md)
</dt> </dl>

 

 



