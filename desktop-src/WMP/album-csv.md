---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player Online Stores album.csv
- Online Stores, album.csv
- Geben Sie 1 Online Stores, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f8b71dc080e6983817d4e6f146249875887ed9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338577"
---
# <a name="albumcsv"></a>album.csv

Diese Datei enthält einen Eintrag für jedes im Katalog enthaltene Album. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Alle Felder in album.csv sind erforderlich.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



| Feld             | Format                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumId           | Nicht negative ganze Zahl. Beispiel: 789456<br/>                          | Der Bezeichner für das-Album, der innerhalb album.csv eindeutig ist. Muss kleiner als 2 ^ 32 sein.                                                                                                                                                                           |
| Albenname         | Unicode-Zeichenfolge. Beispiel: größte Treffer<br/>                         | Titel des Albums                                                                                                                                                                                                                                          |
| Albumartist       | Nicht negative ganze Zahl. Beispiel: 34331<br/>                           | ArtistId des Künstlers. Es ist nur ein Wert zulässig. Kann die ID von "verschiedene Künstler" oder ähnlich sein.                                                                                                                                                    |
| Albumlabel        | Unicode-Zeichenfolge. Muss leer sein.                                         | Wird in dieser Version nicht verwendet. Muss leer sein.                                                                                                                                                                                                           |
| ReleaseDate       | Unicode-Zeichenfolge im Format yyyy-mm-dd. Beispiel: 2005-0-0<br/>        | Veröffentlichungsdatum. Der Wert 0 ist für Tag oder Monat zulässig.                                                                                                                                                                                               |
| Albumprice        | Unicode-stringExample: $12,49<br/>                                 | Album Preis. Das Währungssymbol sollte eingeschlossen werden. Die leere Zeichenfolge 0 und-haben eine besondere Bedeutung. Eine leere Zeichenfolge weist auf einen unbekannten Preis hin. "0" gibt an, dass der Track kostenlos ist. Ein Bindestrich ("-") gibt an, dass das Album nicht erworben werden kann. |
| Linkedgenreid     | Nicht negative ganze Zahl. Beispiel: 12<br/>                              | ID des primären Genres für das Album. Es ist nur ein Wert zulässig.                                                                                                                                                                                        |
| Linkedsubgenreids | Format: n; n; n; Beispiel: 32; 44; 663;<br/>                             | Liste der zugeordneten Subgenre-IDs. Am Ende der Liste ist ein nachfolgendes Semikolon zulässig.                                                                                                                                                             |
| Beliebtheit        | Kann eine nicht negative ganze Zahl oder ein Dezimalwert sein. Beispiel: 1256,24<br/> | Die vom Dienst festgelegte beliebtheitsbewertung. Kann die Rangfolge dieses Albums in der Liste der durch die Beliebtheit sortierten Alben sein. 0 ist zulässig.                                                                                                              |
| Isrecentlyadded   | Boolesch. Kann 0 oder 1 sein.                                                  | Flag, das anzeigt, dass das Album vor kurzem dem Dienst hinzugefügt wurde.                                                                                                                                                                    |
| Isfeatured        | Boolesch. Kann 0 oder 1 sein.                                                  | Flag, das anzeigt, dass es sich um ein gefeaturealbum handelt                                                                                                                                                                                                      |
| Editorialglyph    | Nicht negative ganze Zahl. Muss 0 sein.                                       | Nicht verwendet ist die Freigabe. Muss 0 sein.                                                                                                                                                                                                                    |
| Feedsareavailable | Boolesch. Kann 0 oder 1 sein.                                                  | Wird in dieser Version nicht verwendet. Muss 0 sein.                                                                                                                                                                                                               |



 

 

 





