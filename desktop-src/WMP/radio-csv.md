---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player,radio.csv
- Onlineshops,radio.csv
- Geben Sie 1 Onlineshops ein, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b473bfaa960dd499fae7eb309d02ccbd693b70061d0975c58357bd72e9dcc410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002940"
---
# <a name="radiocsv"></a>radio.csv

Diese Datei enthält Einträge für jeden Im Katalog enthaltenen Radiofeed. Jeder Eintrag ist eine Zeile, die aus den Feldern mit Tabstopptrennzeichen besteht, die in der folgenden Tabelle beschrieben sind. Felder müssen in der aufgeführten Reihenfolge angezeigt werden.

Die Spalte Format in der folgenden Tabelle beschreibt die Formatierung der einzelnen Unicode-Textfelder. Er bezieht sich nicht auf den Datentyp des Inhalts. Wenn beispielsweise Integer in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen ganzen Zahl darstellt.



| Feld              | Erforderlich | Format                                                                                                               | BESCHREIBUNG                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Ja      | Nicht negative ganze Zahl.                                                                                                | ID für den Radiofeed, der innerhalb des radio.csv.                                                                             |
| RadioTitle         | Ja      | Unicode-Zeichenfolge. Beispiel: Wichtige Treffer<br/>                                                                    | Titel des Radiofeeds.                                                                                                                  |
| RadioSubtitle      | Nein       | Unicode-Zeichenfolge. Beispiel: Top 40.                                                                                     | Untertitel des Radiofeeds. Häufig ein Genre- oder Untergenrename.                                                                               |
| Programmierer         | Ja      | Unicode-Zeichenfolge. Beispiel: Terri Lee Duffy                                                                             | Name des Radiofeed-Programmierers. Es wird empfohlen, dieses Feld nicht länger als 32 Zeichen zu sein.                                     |
| PrimaryGenre       | Ja      | Nicht negative ganze Zahl.                                                                                                | Die ID des primären Genre. Es ist nur ein Wert zulässig.                                                                            |
| Stimmung               | Ja      | Unicode-Zeichenfolge. Beispiel: Fun; amiable; - und -3000 ; Üppigen<br/>                                       | Eine Reihe von Adjektiven, die die Musik beschreiben. Kein nach dem letzten Adjektiv nach dem letzten Semikolon.                                    |
| Kategorie           | Ja      | Unicode-Zeichenfolge                                                                                                       | Wird in dieser Version nicht verwendet. Sollte leer sein.                                                                                         |
| BESCHREIBUNG        | Nein       | Unicode-Zeichenfolge. Beispiel: Upbeat party-friendly music from the tried-and-true fans who will't en en 10000 (Beispiel: Upbeat party-friendly music from the tried-and-true fans who will't en 100000000000000<br/> | Benutzerfreundliche Beschreibung für die Anzeige auf Eigenschaftenseiten. Es wird empfohlen, dieses Feld nicht länger als 256 Zeichen zu sein.                   |
| Beliebtheit         | Ja      | Nicht negativer Ganzzahl- oder Dezimalwert. Beispiel: 31<br/>                                                         | Rangfolge der Beliebtheit bei Radiofeeds. Kann 0 sein.                                                                                    |
| StarRating         | Nein       | Float.Example: 3.21<br/>                                                                                       | Optional. Der Wert, in der Regel zwischen 0 und 5, wird zur Anzeige auf der Benutzeroberfläche auf das nächste 1/4 gerundet.                   |
| IsSubscriptionOnly | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob der Feed nur nach Abonnement verfügbar ist.                                                                      |
| IsRecentlyAdded    | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob dieser Feed vor Kurzem hinzugefügt wurde.                                                                                    |
| IsFeatured         | Ja      | Boolesch. Kann 0 oder 1 sein.                                                                                              | Gibt an, ob der Feed als Feature verwendet wird.                                                                                            |
| EditorialGlyph     | Ja      | Nicht negative ganze Zahl. Muss 0 sein.                                                                                   | Wird in dieser Version nicht verwendet. Muss 0 sein.                                                                                             |
| SortOrderRank      | Ja      | Nicht negative ganze Zahl.                                                                                                | Kann verwendet werden, um die Sortierreihenfolge zu bestimmen, wenn alle Stationen auf der Benutzeroberfläche aufgeführt werden. Sollte 0 sein, wenn dieses Feld nicht verwendet wird. |



 

 

 





