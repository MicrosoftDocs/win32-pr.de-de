---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Onlineshops,artist.csv
- Onlineshops,artist.csv
- Geben Sie 1 Onlineshops ein, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4192d0817740ac872d1c08989f2f57b4715d65fea6b9a6c9a199dcdabe267e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583042"
---
# <a name="artistcsv"></a>artist.csv

Diese Datei enthält einen Eintrag für jeden Interpreten im Katalog. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Alle Felder in artist.csv sind erforderlich.

Die Spalte Format in der folgenden Tabelle beschreibt die Formatierung der einzelnen Unicode-Textfelder. Er bezieht sich nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.



| Feld                  | Format                                            | BESCHREIBUNG                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| InterpretID               | Nicht negative ganze Zahl. Beispiel: 65832              | Eindeutiger Bezeichner für den Interpreten, eindeutig innerhalb artist.csv. Muss kleiner als 2^32 sein.                        |
| ArtistName             | Unicode-Zeichenfolge. Beispiel: Don Funk<br/>       | Anzeigename für den Interpreten.                                                                               |
| LinkedGenreID          | Nicht negative ganze Zahl. Beispiel: 313<br/>      | GenreID des primären Genre des Interpreten. Muss ein Hauptgenre und kein Untergeordneter sein. Es ist nur ein Wert zulässig. |
| LinkedSimilarArtistIDs | –                                               | Wird in dieser Version nicht verwendet. Sollte leer sein.                                                                 |
| Beliebtheit             | Kann eine ganze Zahl oder ein Dezimalwert sein. Beispiel: 1252.25 | Rangfolge der Beliebtheit. Kann die Position in der Liste sein, wenn sie nach Beliebtheit sortiert ist.                             |
| FeedsAvailable         | Boolesch. Format: \[ 0 \| 1 \] Beispiel: 0<br/>    | Wird in dieser Version nicht verwendet. Sollte leer sein.                                                                 |



 

 

 





