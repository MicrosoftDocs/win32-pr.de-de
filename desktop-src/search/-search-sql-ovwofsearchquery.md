---
description: Die Windows Search-strukturierte Abfragesprache (SQL) ähnelt einer Standardabfrage SQL.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Übersicht über Windows Search SQL Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f34f321bef35ab9f5198345a2630d20b80275b794f53a0c47aabf7667f2e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594740"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Übersicht über Windows Search SQL Syntax

Die Windows Search-strukturierte Abfragesprache (SQL) ähnelt einer Standardabfrage SQL. Dies wird in den folgenden beiden Syntaxen gezeigt:


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

Im folgenden Abfragebeispiel werden die Werte für Seitenanzahl und Erstellungsdatum für alle Dokumente zurückgegeben, die über mehr als 50 Seiten verfügen. Sortiert ist die Reihenfolge der Seitenanzahl aufsteigend.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

Die Windows Search-Abfragesyntax unterstützt viele Optionen und ermöglicht kompliziertere Abfragen.

In der folgenden Tabelle werden die einzelnen Klauseln in den SELECT- oder GROUP ON-Anweisungen und die unterstützten Features beschrieben.

| Klausel                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GROUP ON... Über...](-search-sql-group-on-over.md) | Gibt an, wie von der Abfrage zurückgegebene Ergebnisse gruppiert werden. Sie können die Bereiche angeben, nach denen gruppiert werden soll, und mehrere Spalten für die Gruppierung angeben. Beispielsweise können Sie Ergebnisse über einen Bereich von Dateigrößen (Größe < 100, 100 <= Größe < 1000; 1000 <= Größe) und Schachtelungsgruppierungen gruppieren.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Gibt die von der Abfrage zurückgegebenen Spalten an.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Gibt den zu durchsuchenden Computer und Katalog an.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Gibt an, was ein übereinstimmendes Dokument ausmacht. Diese Klausel verfügt über viele Optionen, die eine umfassende Kontrolle über die Suchbedingungen ermöglichen. Beispielsweise können Sie mit Wörtern, Ausdrücken, Flexionswortformen, Zeichenfolgen, numerischen und bitweisen Werten und mehrwertigen Arrays abgleichen. Sie können auch statistische Gewichtungen auf die Abgleichsbedingungen anwenden und Abgleichsbedingungen mit booleschen Operatoren kombinieren. |
| [ORDER BY](-search-sql-orderby.md)                 | Gibt die Sortierreihenfolge für die von der Abfrage zurückgegebenen Ergebnisse an. Sie können mehr als ein Feld angeben, nach dem die Ergebnisse sortiert werden, und Sie können aufsteigende oder absteigende Reihenfolge verwenden.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Codebeispiele

Das WSSQL-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über SQL. Das WSOleDB-Codebeispiel veranschaulicht Active Template Library (ATL) OLE DB Zugriff auf Windows Search-Anwendungen und zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus Windows Search. Beide Beispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

### <a name="reference"></a>Verweis

[Literale](-search-sql-literals.md)

[Verwenden von lokalisierten Suchen](-search-sql-usinglocsearches.md)

[Grundlegendes zu Relevanzwerten](-search-sql-understandingrelevancevalues.md)

[Eigenschaftenzuordnungen](-search-3x-wds-propertymappings.md)

[Erweiterte Abfragesyntax](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Konzept

[SQL Erweiterungen in Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL Nicht verfügbare Features in Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identifiers (Bezeichner)](-search-sql-identifiers.md)

[Empfindlichkeit der Fall bei Suchvorgängen](-search-sql-casesensitivityinsearches.md)

[Diakritische Empfindlichkeit in Suchvorgängen](-search-sql-accentinsensitivitysearches.md)

[Umwandeln des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md)

[Datentypzuordnungen](-search-sql-datatypemappings.md)
