---
description: Der Windows Search-Structured Query Language (SQL) ähnelt einer SQL-Standard Abfrage.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Übersicht über die SQL-Syntax von Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041629"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Übersicht über die SQL-Syntax von Windows Search

Der Windows Search-Structured Query Language (SQL) ähnelt einer SQL-Standard Abfrage. Dies wird in den folgenden beiden Syntaxen angezeigt:


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

Im folgenden Abfrage Beispiel werden die Werte für die Seitenanzahl und den Erstellungsdatum für alle Dokumente zurückgegeben, die mehr als 50 Seiten enthalten, sortiert ist die aufsteigende Reihenfolge der Seitenanzahl.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

Die Syntax der Windows-Suchabfrage unterstützt viele Optionen und ermöglicht so kompliziertere Abfragen.

In der folgenden Tabelle werden die einzelnen-Klauseln in der SELECT-oder Group on-Anweisung und die unterstützten Funktionen beschrieben.

| Klausel                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gruppieren nach... Über...](-search-sql-group-on-over.md) | Gibt an, wie die von der Abfrage zurückgegebenen Ergebnisse gruppiert werden. Sie können die Bereiche angeben, nach denen gruppiert werden soll, und mehr als eine Spalte für die Gruppierung angeben. Beispielsweise können Sie Ergebnisse in einem Bereich von Dateigrößen gruppieren (Größe < 100, 100 <= Größe < 1000; 1000 <= Größe) und Schachteln von Gruppierungen.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Gibt die von der Abfrage zurückgegebenen Spalten an.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Gibt den zu durchsuchenden Computer und Katalog an.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Gibt an, was ein entsprechendes Dokument ausmacht. Diese Klausel verfügt über viele Optionen und ermöglicht eine umfassende Kontrolle über die Suchbedingungen. Beispielsweise können Sie mit Wörtern, Ausdrücken, flektiven Wort Formularen, Zeichen folgen, numerischen und bitweisen Werten und mehrwertigen Arrays vergleichen. Sie können auch statistische Gewichtungen auf die übereinstimmenden Bedingungen anwenden und übereinstimmende Bedingungen mit booleschen Operatoren kombinieren. |
| [ORDER BY](-search-sql-orderby.md)                 | Gibt die Sortierreihenfolge für die von der Abfrage zurückgegebenen Ergebnisse an. Sie können mehr als ein Feld angeben, in dem die Ergebnisse sortiert werden, und Sie können aufsteigende oder absteigende Reihenfolge verwenden.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Codebeispiele

Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über SQL. Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus Windows Search. Beide Beispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Referenz

[Literale](-search-sql-literals.md)

[Verwenden lokalisierter Suchvorgänge](-search-sql-usinglocsearches.md)

[Verstehen von relevanzwerten](-search-sql-understandingrelevancevalues.md)

[Eigenschafts Zuordnungen](-search-3x-wds-propertymappings.md)

[Erweiterte Abfragesyntax](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Konzept

[SQL-Erweiterungen in Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.](-search-sql-featuresunavailableinspssearch.md)

[Identifiers (Bezeichner)](-search-sql-identifiers.md)

[Groß-/Kleinschreibung in suchen](-search-sql-casesensitivityinsearches.md)

[Diakritische Empfindlichkeit bei Such Vorgängen](-search-sql-accentinsensitivitysearches.md)

[Umwandeln des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md)

[Datentypzuordnungen](-search-sql-datatypemappings.md)
