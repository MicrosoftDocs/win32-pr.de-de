---
description: Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden von der WHERE-Klausel angegeben.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: WHERE-Klausel (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462402"
---
# <a name="where-clause-windows-search"></a>WHERE-Klausel (Windows Search)

Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden von der WHERE-Klausel angegeben. Auf der höchsten Ebene gibt es zwei Teile der WHERE-Klauselsyntax:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



Der optionale <\_ Gruppenalias> Teil der -Klausel vereinfacht komplexe Abfragen, indem einer Gruppe von einer oder mehreren Spalten ein Alias zugewiesen wird. Dies kann die Lesbarkeit komplexer Abfragen verbessern, die in mehreren durch URLs angegebenen Spalten nach denselben Informationen suchen. Weitere Informationen zu Gruppenaliasen finden Sie unter [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).

Der <search condition> Teil der WHERE-Klausel ist ein oder mehrere Suchprädikate, die Übereinstimmungskriterien für die Suche angeben. Bei Suchprädikaten handelt es sich um Ausdrücke, die eine Tatsache zu einem Bestimmten Wert bestätigen.

Das Ergebnis einer Suchbedingung ist ein boolescher Wert, entweder **TRUE,** wenn das Dokument die angegebenen Suchbedingungen erfüllt, oder **FALSE,** wenn dies nicht der Fall ist. Wenn das Ergebnis **TRUE** ist, wird das Dokument zurückgegeben. Wenn das Ergebnis **FALSE** ist, wird das Dokument nicht zurückgegeben. Dokumenten, die in einer Microsoft Windows Search-Abfrage zurückgegeben werden, werden Rangwerte entsprechend ihrer Übereinstimmung mit den Suchbedingungen zugewiesen. Jede der Abfragesuchbedingungen kann eine [RANKBY-Klausel](-search-sql-rankby.md) enthalten, die das Ändern der zurückgegebenen Rangwerte unterstützt.

Die [ReuseWhere-Funktion](-search-sql-reusewhere.md) macht mehrere Abfragen effizienter, die einige der gleichen Suchbedingungen verwenden. Die WHERE-Klausel in einer Abfrage gibt den Satz von Elementen an, die in einer Abfrage übereinstimmen. Nachfolgende Abfragen können die Für die vorherige Auswertung ausgeführte Arbeit mithilfe der ReuseWhere-Funktion in der neuen WHERE-Abfrageklausel freigeben.

## <a name="search-predicates"></a>Suchprädikate

Eine Suchbedingung besteht aus einem oder mehreren Prädikaten oder Suchbedingungen, die beschreiben, wonach der Benutzer sucht (z.B. WHERE System.DateCreated >'2006-04-19'). Suchprädikate können mithilfe der logischen Operatoren **AND,** **OR** oder **NOT** kombiniert werden. Der optionale unäre Operator **NOT** kann nur mit **AND** und nur zum Negieren des logischen Werts eines Prädikats oder einer Suchbedingung verwendet werden. Sie können logische Begriffe mithilfe von Klammern gruppieren und schachteln.

Die folgende Tabelle zeigt die Rangfolge für die logischen Operatoren.



| Reihenfolge (Rangfolge) | Logischer Operator |
|--------------------|------------------|
| Erste (höchste)    | **NOT**          |
| Second             | **AND**          |
| Dritte (niedrigste)     | **OR**           |



 

Logische Operatoren desselben Typs sind assoziativ, und es gibt keine angegebene Berechnungsreihenfolge. Beispielsweise können (A **UND** B) **AND** (C **UND** D) (A **UND** D) **UND** (B **UND** C) ohne Änderung des logischen Ergebnisses berechnet werden.

> [!IMPORTANT]
>
> Falsch: WHERE **NOT** CONTAINS ('computer')
>
> Richtig: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')

 

Bei komplexen Abfragen sollten Sie übereinstimmungen in einigen Spalten mehr Aufmerksamkeit als in anderen spalten. Wenn Sie beispielsweise nach Dokumenten suchen, die "Softwareentwurf" besprechen, ist es wahrscheinlicher, den Suchbegriff im Dokumenttitel zu finden, als die einzelnen Wörter im Text des Dokuments zu finden. Um die Rangfolge von Dokumenten auf diese Weise zu beeinflussen, unterstützt die Abfragesprache Microsoft Windows Search die Gewichtung der Suchbedingungen. Weitere Informationen zur Spaltengewichtung finden Sie unter [CONTAINS-Prädikat](-search-sql-contains.md) und [FREETEXT-Prädikat.](-search-sql-freetext.md)

Es gibt drei Gruppen von Suchprädikaten in Windows Search: Volltext-, Nicht-Volltext- und Ordnertiefesuchvorgänge. Volltextsuchprädikate stimmen in der Regel mit der Bedeutung von Inhalt, Titel und anderen Spalten überein und unterstützen linguistische Übereinstimmungen (z. B. alternative Wortformen, Ausdrücke und Näherungssuche). Im Gegensatz dazu stimmen Prädikate ohne Volltextsuche mit dem Wert der angegebenen Spalten überein und enthalten keine spezielle linguistische Verarbeitung, bieten jedoch in mehreren Fällen zeichenbasierte Musterübereinstimmungen. Ordnertiefeprädikate beschränken den Suchbereich auf einen angegebenen Pfad.

> [!Note]  
> Wenn die Abfrage ein Dokument zurückgibt, weil ein Nicht-Volltextprädikat für dieses Dokument zu **TRUE** ausgewertet wird, wird der Rangwert als 1000 berechnet. Mithilfe der [Rangfolgekoersionsfunktion](-search-sql-rankby.md) kann der Rangwert geändert werden.

 

In den folgenden Tabellen werden die Prädikate für die Suche nach Volltext, Nicht-Volltext und Ordnertiefe beschrieben.



| Volltextprädikat                  | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Unterstützt komplexe Suchen nach Begriffen in Dokumenttextspalten (z. B. Titel, Inhalt). Kann nach inflektierten Formen der Suchbegriffe suchen, die Nähe der Begriffe testen und logische Vergleiche durchführen. Suchbegriffe können Platzhalterzeichen enthalten. |
| [FREETEXT](-search-sql-freetext.md) | Sucht nach Dokumenten, die der Bedeutung des Suchbegriffs entsprechen. Verwandte Wörter und ähnliche Ausdrücke stimmen überein, wobei die Rangfolgespalte basierend darauf berechnet wird, wie genau das Dokument mit dem Suchbegriff übereinstimmt. Suchbegriffe dürfen keine Platzhalterzeichen enthalten.  |



 



| Nicht-Volltextprädikat                                                    | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Spaltenwerte werden mithilfe eines einfachen Musterabgleichs mit Platzhalterzeichen verglichen.                                                                                                    |
| [Literalwertvergleich](-search-sql-literalvaluecomparison.md)         | Spaltenwerte werden mit Zeichenfolgen-, Datums-, Zeitstempel-, numerischen und anderen Literalwerten verglichen. Dieses Prädikat unterstützt Gleichheit und Gleichheit, z. B. größer als und kleiner als. |
| [Mehrwertige Vergleiche (ARRAY)](-search-sql-multivaluedcomparisons.md) | Mehrwertige Spalten werden mit einem mehrwertigen Array von Literalen verglichen.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Spaltenwerte, die für das Dokument nicht definiert sind,  können mithilfe des NULL-Prädikats erkannt werden.                                                                                    |



 



| Ordnertiefe                             | BESCHREIBUNG                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Umfang](-search-sql-folderdepth.md)     | Führt einen tiefen Durchlauf des angegebenen Pfads aus, einschließlich des spezifischen Ordners und aller Unterordner. |
| [Verzeichnis](-search-sql-folderdepth.md) | Führt einen flachen Durchlauf des angegebenen Pfads durch und durchsucht nur den bestimmten Ordner.            |



 

## <a name="examples"></a>Beispiele

Beispiele für die WHERE-Klausel finden Sie in den einzelnen Prädikatthemen, die in der vorherigen Tabelle verknüpft sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[ReuseWhere-Funktion](-search-sql-reusewhere.md)
</dt> <dt>

[Rowset-Eigenschaften](-search-sql-rowset-properties.md)
</dt> <dt>

[FROM-Klausel](-search-sql-from.md)
</dt> <dt>

[Übersicht über die Syntax für SQL suchen](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH – AS-Gruppenaliasprädikat](-search-sql-with-as.md)
</dt> <dt>

[SCOPE- und DIRECTORY-Prädikate](-search-sql-folderdepth.md)
</dt> <dt>

[RANK BY-Klausel](-search-sql-rankby.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



