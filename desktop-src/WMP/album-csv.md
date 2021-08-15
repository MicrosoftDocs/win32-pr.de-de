---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player Onlineshops,album.csv
- Onlineshops,album.csv
- Geben Sie 1 Onlineshops ein, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750926a3d01f8d65d7ed11c69436049e39ea3dabf0e446ede8a8c9dcecc53bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004200"
---
# <a name="albumcsv"></a>album.csv

Diese Datei enthält einen Eintrag für jedes im Katalog enthaltene Album. Jeder Eintrag ist eine Zeile, die aus den Feldern mit Tabstopptrennzeichen besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Alle Felder in album.csv sind erforderlich.

Die Spalte Format in der folgenden Tabelle beschreibt die Formatierung der einzelnen Unicode-Textfelder. Er bezieht sich nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.



| Feld             | Format                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Nicht negative ganze Zahl. Beispiel: 789456<br/>                          | Bezeichner für das Album, eindeutig innerhalb album.csv. Muss kleiner als 2^32 sein.                                                                                                                                                                           |
| AlbumName         | Unicode-Zeichenfolge. Beispiel: Größte Treffer<br/>                         | Titel des Albums                                                                                                                                                                                                                                          |
| AlbumArtist       | Nicht negative ganze Zahl. Beispiel: 34331<br/>                           | InterpretID des Interpreten. Es ist nur ein Wert zulässig. Kann die ID von "Various Artist" oder ähnliches sein.                                                                                                                                                    |
| AlbumLabel        | Unicode-Zeichenfolge. Sollte leer sein.                                         | Wird in dieser Version nicht verwendet. Sollte leer sein.                                                                                                                                                                                                           |
| Released       | Unicode-Zeichenfolge im Format YYYY-MM-DD. Beispiel: 2005-0-0<br/>        | Veröffentlichungsdatum. Der Wert 0 ist für Tag oder Monat zulässig.                                                                                                                                                                                               |
| AlbumPrice        | Unicode-ZeichenfolgeBeispiel: 12,49 USD<br/>                                 | Albumpreis. Das Währungssymbol sollte enthalten sein. Die leere Zeichenfolge 0 und - haben eine besondere Bedeutung. Eine leere Zeichenfolge gibt einen unbekannten Preis an. "0" gibt an, dass die Spur frei ist. Ein Bindestrich ("-") gibt an, dass das Album nicht erworben werden kann. |
| LinkedGenreID     | Nicht negative ganze Zahl. Beispiel: 12<br/>                              | ID des primären Genre für das Album. Es ist nur ein Wert zulässig.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Format: n;n;n; Beispiel: 32;44;663;<br/>                             | Liste der zugeordneten Untergenre-IDs. Am Ende der Liste ist ein nachhingendes Semikolon zulässig.                                                                                                                                                             |
| Beliebtheit        | Kann ein nicht negativer Ganzzahl- oder Dezimalwert sein. Beispiel: 1256.24<br/> | Vom Dienst ermittelte Beliebtheitsbewertung. Kann die Rangfolge dieses Albums in der Liste der Nach Beliebtheit sortierten Albums sein. 0 ist zulässig.                                                                                                              |
| IsRecentlyAdded   | Boolesch. Kann 0 oder 1 sein.                                                  | Flag, um anzugeben, dass das Album vor Kurzem hinzugefügt wurde, wie vom Dienst festgelegt.                                                                                                                                                                    |
| IsFeatured        | Boolesch. Kann 0 oder 1 sein.                                                  | Flag, um anzugeben, dass es sich um ein ausgewähltes Album handelt.                                                                                                                                                                                                      |
| EditorialGlyph    | Nicht negative ganze Zahl. Muss 0 sein.                                       | Nicht verwendet ist release. Muss 0 sein.                                                                                                                                                                                                                    |
| FeedsAreAvailable | Boolesch. Kann 0 oder 1 sein.                                                  | Wird in dieser Version nicht verwendet. Muss 0 sein.                                                                                                                                                                                                               |



 

 

 





