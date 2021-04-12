---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player Online Stores radio.csv
- Online Stores, radio.csv
- Geben Sie 1 Online Stores, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310708"
---
# <a name="radiocsv"></a>radio.csv

Diese Datei enthält Einträge für jeden Radio Feed, der im Katalog enthalten ist. Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird. Er verweist nicht auf den Datentyp des Inhalts. Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.



| Feld              | Erforderlich | Format                                                                                                               | BESCHREIBUNG                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Radio ID            | Ja      | Nicht negative ganze Zahl.                                                                                                | ID für den Radio Feed, der innerhalb radio.csv eindeutig ist.                                                                             |
| Radio Title         | Ja      | Unicode-Zeichenfolge. Beispiel: wichtige Treffer<br/>                                                                    | Titel des Radio Feeds.                                                                                                                  |
| Radio-Untertitel      | Nein       | Unicode-Zeichenfolge. Beispiel: Top 40.                                                                                     | Untertitel des Radio Feeds. Häufig ein Genre-oder Subgenre Name.                                                                               |
| ERS         | Ja      | Unicode-Zeichenfolge. Beispiel: Terri Lee Duffy                                                                             | Der Name des Radio-Feed-Programmierers. Es wird empfohlen, dass dieses Feld nicht länger als 32 Zeichen ist.                                     |
| Primarygenre       | Ja      | Nicht negative ganze Zahl.                                                                                                | Die ID des primären Genres. Es ist nur ein Wert zulässig.                                                                            |
| Mood               | Ja      | Unicode-Zeichenfolge. Beispiel: Spaß; kann nicht angezeigt werden. energetische voller schwän<br/>                                       | Eine Reihe von Adjektiven, die die Musik beschreiben. Kein nachfolgender Semikolon nach dem letzten Adjektiv.                                    |
| Category           | Ja      | Unicode-Zeichenfolge                                                                                                       | Wird in dieser Version nicht verwendet. Muss leer sein.                                                                                         |
| BESCHREIBUNG        | Nein       | Unicode-Zeichenfolge. Beispiel: Upbeat Party-Friendly Musik von den versuchten und echten Künstlern, die nicht enttäuschen.<br/> | Benutzerfreundliche Beschreibung für die Anzeige auf Eigenschaften Seiten. Es wird empfohlen, dass dieses Feld nicht länger als 256 Zeichen ist.                   |
| Beliebtheit         | Ja      | Eine nicht negative ganze Zahl oder ein Dezimalwert. Beispiel: 31<br/>                                                         | Beliebtheits Rangfolge zwischen Radio Feeds. Kann 0 sein.                                                                                    |
| Star Rating         | Nein       | Float. Beispiel: 3,21<br/>                                                                                       | Dies ist optional. Der Wert, der normalerweise zwischen 0 und 5 liegt, wird für die Anzeige auf der Benutzeroberfläche auf den nächstgelegenen 1/4 gerundet.                   |
| Isabonptiononly | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob der Feed nur durch Abonnement verfügbar ist.                                                                      |
| Isrecentlyadded    | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob dieser Feed kürzlich hinzugefügt wurde.                                                                                    |
| Isfeatured         | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob der Feed angezeigt wird.                                                                                            |
| Editorialglyph     | Ja      | Nicht negative ganze Zahl. Muss 0 sein.                                                                                   | Wird in dieser Version nicht verwendet. Muss 0 sein.                                                                                             |
| Sorrenderrank      | Ja      | Nicht negative ganze Zahl.                                                                                                | Kann zum Bestimmen der Sortierreihenfolge verwendet werden, wenn alle Stationen in der Benutzeroberfläche aufgelistet sind. Sollte 0 sein, wenn dieses Feld nicht verwendet wird. |



 

 

 





