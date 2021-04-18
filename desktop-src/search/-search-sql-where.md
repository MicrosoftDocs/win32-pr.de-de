---
description: Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden durch die WHERE-Klausel angegeben.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: WHERE-Klausel (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344674"
---
# <a name="where-clause-windows-search"></a>WHERE-Klausel (Windows-Suche)

Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden durch die WHERE-Klausel angegeben. Auf der höchsten Ebene gibt es zwei Teile der Syntax der WHERE-Klausel:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



Der optionale <\_ Gruppenalias> Teil der-Klausel vereinfacht komplexe Abfragen, indem einer Gruppe von mindestens einer Spalte ein Alias zugewiesen wird. Dies kann die Lesbarkeit komplexer Abfragen verbessern, die über mehrere durch URLs angegebene Spalten hinweg nach denselben Informationen suchen. Weitere Informationen zu Gruppen Aliasen finden Sie unter [with-as Group Alias Predicate](-search-sql-with-as.md).

Der <search condition> Teil der WHERE-Klausel ist ein oder mehrere Such Prädikate, die übereinstimmende Kriterien für die Suche angeben. Such Prädikate sind Ausdrücke, die einige Fakten über einen Wert bestätigen.

Das Ergebnis einer Such Bedingung ist ein boolescher Wert, entweder **true** , wenn das Dokument die angegebenen Suchbedingungen erfüllt, oder **false** , wenn dies nicht der Fall ist. Wenn das Ergebnis **true** ist, wird das Dokument zurückgegeben. Wenn das Ergebnis **false** ist, wird das Dokument nicht zurückgegeben. Bei Dokumenten, die in einer Microsoft Windows Search-Abfrage zurückgegeben werden, werden Rang Werte entsprechend der Übereinstimmung der Suchbedingungen zugewiesen. Jede der Abfrage Suchbedingungen kann eine [rankby](-search-sql-rankby.md) -Klausel enthalten, die das Ändern der zurückgegebenen Rang Werte unterstützt.

Die [reusewhere-Funktion](-search-sql-reusewhere.md) macht mehrere Abfragen, die die gleichen Suchbedingungen verwenden, effizienter. Die WHERE-Klausel in einer Abfrage gibt den Satz von Elementen an, die in einer Abfrage gefunden werden. Nachfolgende Abfragen können die Arbeit, die für die vorherige Auswertung ausgeführt wird, mithilfe der Funktion reusewhere in der neuen Abfrage WHERE-Klausel freigeben.

## <a name="search-predicates"></a>Such Prädikate

Eine Such Bedingung besteht aus einem oder mehreren Prädikaten oder Suchbedingungen, die beschreiben, wie der Benutzer sucht (z. b. wenn System. DateCreated > "2006-04-19"). Such Prädikate können mit den logischen Operatoren **and**, **or** oder **Not** kombiniert werden. Der optionale unäre Operator **Not** kann nur mit **und** und nur verwendet werden, um den logischen Wert eines Prädikats oder einer Such Bedingung zu negieren. Sie können Klammern verwenden, um logische Begriffe zu gruppieren und zu schachteln.

Die folgende Tabelle zeigt die Rangfolge der logischen Operatoren.



| Reihenfolge (Rangfolge) | Logischer Operator |
|--------------------|------------------|
| First (höchste)    | **NOT**          |
| Sekunde             | **AND**          |
| Dritte (niedrigste)     | **OR**           |



 

Logische Operatoren desselben Typs sind assoziativ, und es ist keine Berechnungs Reihenfolge angegeben. Beispielsweise können (a **und** B) **und** (c **und** d) (a **und** d) **und** (B **und** C) ohne Änderung im logischen Ergebnis berechnet werden.

> [!IMPORTANT]
>
> Falsch: Where **Not** enthält (' Computer ')
>
> Richtig: Where enthält ("Software") **und enthält keine** ("Computer").

 

In komplexen Abfragen möchten Sie möglicherweise mehr Akzente in einigen Spalten als in anderen Spalten platzieren. Wenn Sie z. b. nach Dokumenten suchen, in denen "Software Design" erläutert wird, ist die Suche nach dem Suchbegriff im Dokumenttitel wahrscheinlich eine gute Frage, als die einzelnen Wörter im Text des Dokuments zu suchen. Um die Rangfolge von Dokumenten auf diese Weise zu beeinflussen, unterstützt die Microsoft Windows Search-Abfragesprache das Abwägen der Suchbedingungen. Weitere Informationen zur Spalten Gewichtung finden Sie unter [enthält ein Prädikat](-search-sql-contains.md) und ein frei [Text Prädikat](-search-sql-freetext.md).

Es gibt drei Gruppen von Such Prädikaten in Windows Search: Volltext, nicht Volltext und Ordner Tiefe suchen. Prädikate für die Volltextsuche entsprechen in der Regel der Bedeutung von Inhalt, Titel und anderen Spalten und unterstützen die linguistische Übereinstimmung (z. b. Alternative Word-Formulare, Ausdrücke und Near-Suche). Im Gegensatz dazu entsprechen nicht-voll Text Suchprädikate dem Wert der angegebenen Spalten und enthalten keine besondere linguistische Verarbeitung, aber in einigen Fällen bieten Zeichen basierten Musterabgleich. Mit den Prädikaten für die Ordner Tiefe wird der Suchbereich auf einen angegebenen Pfad beschränkt.

> [!Note]  
> Wenn die Abfrage ein Dokument zurückgibt, weil ein nicht-voll Text Prädikat für dieses Dokument **true** ergibt, wird der Rangwert als 1000 berechnet. Durch die Verwendung der Rang Umwandlungs [Funktion](-search-sql-rankby.md) kann der Rangwert geändert werden.

 

In den folgenden Tabellen werden die Prädikate für Volltext-, nicht-Volltext-und Ordner Tiefe-Suche beschrieben.



| Volltext-Prädikat                  | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Unterstützt komplexe Suchvorgänge für Begriffe in Dokument Textspalten (z. b. Titel, Inhalt). Kann nach inflektierte Formen der Suchbegriffe suchen, auf die Nähe der Begriffe testen und logische Vergleiche durchführen. Suchbegriffe können Platzhalter Zeichen enthalten. |
| [FREETEXT](-search-sql-freetext.md) | Sucht nach Dokumenten, die der Bedeutung des Such Ausdrucks entsprechen. Verwandte Wörter und ähnliche Ausdrücke stimmen überein, wobei die Rang Spalte auf der Grundlage der Übereinstimmung des Dokuments mit dem Suchbegriff berechnet wird. Suchbegriffe dürfen keine Platzhalter Zeichen enthalten.  |



 



| Nicht-voll Text Prädikat                                                    | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Spaltenwerte werden mithilfe eines einfachen Musterabgleich mit Platzhaltern verglichen.                                                                                                    |
| [Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)         | Spaltenwerte werden mit Zeichen folgen-, Datums-, Zeitstempel-, numerischen und anderen Literalwerten verglichen. Dieses Prädikat unterstützt Gleichheit und Ungleichheiten wie "größer als" und "kleiner als". |
| [Mehrwertige Vergleiche (Array)](-search-sql-multivaluedcomparisons.md) | Mehrwertige Spalten werden mit einem mehrwertigen Array von literalen verglichen.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Spaltenwerte, die für das Dokument nicht definiert sind, können mithilfe des **null** -Prädikats erkannt werden.                                                                                    |



 



| Ordner Tiefe                             | BESCHREIBUNG                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Umfang](-search-sql-folderdepth.md)     | Führt einen tiefen Durchlauf des angegebenen Pfads aus, einschließlich des jeweiligen Ordners und aller Unterordner. |
| [Befinden](-search-sql-folderdepth.md) | Führt einen flachen Durchlauf des angegebenen Pfads durch und sucht nur nach dem jeweiligen Ordner.            |



 

## <a name="examples"></a>Beispiele

Beispiele für die WHERE-Klausel finden Sie in den Themen zu den einzelnen Prädikaten, die in der obigen Tabelle verknüpft sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Reusewhere-Funktion](-search-sql-reusewhere.md)
</dt> <dt>

[Rowset-Eigenschaften](-search-sql-rowset-properties.md)
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[Übersicht über die SQL-Such Syntax](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH--as Group Alias-Prädikat](-search-sql-with-as.md)
</dt> <dt>

[Bereichs-und Verzeichnis Prädikate](-search-sql-folderdepth.md)
</dt> <dt>

[Rank by-Klausel](-search-sql-rankby.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



