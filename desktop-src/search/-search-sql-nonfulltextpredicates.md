---
description: Die Microsoft Windows Search-Abfragesprache unterstützt sechs Prädikate, die keine Volltextsuche sind. Die in diesem Abschnitt beschriebenen Prädikate sind in der folgenden Tabelle aufgeführt.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Nicht-voll Text Prädikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344264"
---
# <a name="non-full-text-predicates"></a>Nicht-voll Text Prädikate

Die Microsoft Windows Search-Abfragesprache unterstützt sechs Prädikate, die keine Volltextsuche sind. Die in diesem Abschnitt beschriebenen Prädikate sind in der folgenden Tabelle aufgeführt.



| Nicht-voll Text Prädikat                                                    | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alle bitweisen und einige bitweise](all-bitwise.md)                            | Ein Satz von Schlüsselwörtern, bei denen die Bits in einem ganzzahligen Typ getestet werden.                                                                                                               |
| [DateAdd-Funktion](-search-sql-dateadd.md)                                | Führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus. Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.     |
| [LIKE-Prädikat](-search-sql-like.md)                                     | Vergleicht Spaltenwerte mithilfe eines einfachen Musterabgleich mit Platzhalter Zeichen.                                                                                                          |
| [Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)         | Vergleicht Spaltenwerte mit Zeichen folgen-, Datums-, Zeitstempel-, numerischen und anderen Literalwerten. Dieses Prädikat unterstützt Ungleichheiten wie "größer als" (">") und "kleiner als" ("<"). |
| [Mehrwertige Vergleiche (Array)](-search-sql-multivaluedcomparisons.md) | Vergleicht mehrwertige Spalten mit einem mehrwertigen Array von Literalen.                                                                                                                   |
| [NULL-Prädikat](-search-sql-null.md)                                     | Erkennt Spaltenwerte, die für das Dokument nicht definiert sind.                                                                                                                              |



 

> [!IMPORTANT]
> Such Abfragen mit dem **null** -Prädikat können erfordern, dass die Windows-Suche den gesamten Katalog scannt, was die Leistung der Abfrage verlangsamen könnte.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



