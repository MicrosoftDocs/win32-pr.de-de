---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online Stores artist.csv
- Online Stores, artist.csv
- Geben Sie 1 Online Stores, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311351"
---
# <a name="artistcsv"></a>artist.csv

Diese Datei enthält einen Eintrag für jeden Künstler im Katalog. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Alle Felder in artist.csv sind erforderlich.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



| Feld                  | Format                                            | BESCHREIBUNG                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistId               | Nicht negative ganze Zahl. Beispiel: 65832              | Eindeutiger Bezeichner für den in artist.csv eindeutigen Bezeichner. Muss kleiner als 2 ^ 32 sein.                        |
| ArtistName             | Unicode-Zeichenfolge. Beispiel: Don Funk<br/>       | Anzeige Name für den Künstler.                                                                               |
| Linkedgenreid          | Nicht negative ganze Zahl. Beispiel: 313<br/>      | GenreID des primären Genres des Künstlers. Muss ein Haupt Genre und kein unter Genre sein. Es ist nur ein Wert zulässig. |
| Linkedsimilarartistids | –                                               | Wird in dieser Version nicht verwendet. Muss leer sein.                                                                 |
| Beliebtheit             | Kann ein ganzzahliger Wert oder ein Dezimalwert sein. Beispiel: 1252,25 | Rangfolgenbewertung. Kann die Position in der Liste sein, wenn Sie nach Beliebtheit sortiert ist.                             |
| Feedsavailable         | Boolesch. Format: \[ 0 \| 1 \] Beispiel: 0<br/>    | Wird in dieser Version nicht verwendet. Muss leer sein.                                                                 |



 

 

 





