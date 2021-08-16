---
description: Das FREETEXT-Prädikat ist Teil der WHERE-Klausel und unterstützt die Suche nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: FREETEXT-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9fb3d65c1b9dc72ef74c8c6862ccfb778ebbd4149b9e5bf5aca4d36674045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863406"
---
# <a name="freetext-predicate"></a>FREETEXT-Prädikat

Das FREETEXT-Prädikat ist Teil der [WHERE-Klausel](-search-sql-where.md) und unterstützt die Suche nach Wörtern und Ausdrücken in Textspalten. Verwenden Sie das FREETEXT-Prädikat, um Dokumente zu suchen, die Kombinationen der Suchbegriffe enthalten, die über den angegebenen Inhalt oder die angegebenen Spalten verteilt sind. Um den Rangwert abzurufen, schließen Sie System.Search.Rank als Spalte in die SELECT-Anweisung ein. Dies ist eine Rangfolge der Relevanz.

Das FREETEXT-Prädikat weist die folgende Syntax auf:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



Der Volltextspaltenverweis ist optional. Damit können Sie eine einzelne Spalte oder einen [Spaltengruppierungsalias](-search-sql-with-as.md) angeben, mit dem das FREETEXT-Prädikat getestet wird. Wenn die Volltextspalte als "ALL" oder "" angegeben \* wird, werden alle indizierten Texteigenschaften durchsucht. Obwohl die Spalte keine Texteigenschaft sein muss, sind die Ergebnisse möglicherweise bedeutungslos, wenn die Spalte ein anderer Datentyp ist. Der Spaltenname kann entweder ein regulärer oder ein durch Trennzeichen getrennter [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen. Wenn keine Volltextbedingung angegeben wird, wird die Spalte Inhalt verwendet, die den Text des Dokuments darstellt.

Sie können ein Suchschema angeben, um die entsprechende Wörterpause und die entsprechenden Flexionsformen für die Suchabfrage zu identifizieren. Gültige Gebietsschemawerte sind ein Windows LCID (Standard Language Code Identifier). Beispielsweise ist 1033 die LCID für USA-Englisch. Platzieren Sie die LCID als letztes Element in den Klammern der FREETEXT-Klausel. Wichtige Informationen zu Suchen und Sprachen finden Sie unter [Verwenden von lokalisierten Suchvorgängen.](-search-sql-usinglocsearches.md)

> [!Note]  
> Das Standardsuchschema ist das Standardschema des Systems.

 

Sie müssen den Teil der Freitextbedingung in einfache Anführungszeichen einschließen und aus einem oder mehreren Suchbegriffen bestehen. Das FREETEXT-Prädikat unterstützt keine logischen Vorgänge. Um nach einem Ausdruck zu suchen, als wäre es ein einzelnes Wort, schließen Sie den Ausdruck in doppelte Anführungszeichen ein.

Wenn Sie das FREETEXT-Prädikat verwenden, geben die Suchergebnisse Dokumente zurück, die alle Suchbegriffe enthalten. Die Begriffe müssen nicht in einer bestimmten Reihenfolge angezeigt werden. Dokumente, die mehr Suchbegriffe enthalten, weisen höhere Rangfolgespaltenwerte auf.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird nach Dokumenten gesucht, die "Computer", "Software", "Hardware" oder Kombinationen dieser Wörter enthalten:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Sie können im selben FREETEXT-Prädikat nicht sowohl den Einzelwortabgleich als auch den Ausdrucksabgleich verwenden.

 

Beim Ausführen von Abfragen mit Contractions müssen Sie das Anführungszeichen in der Contraction mit Escapezeichen versehen, wenn Sie FREETEXT verwenden, aber nicht, wenn Sie CONTAINS verwenden.

Die folgende Syntax schlägt beispielsweise fehl:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



Die richtige Syntax enthält zwei einfache Anführungszeichen, kein doppeltes Anführungszeichen.

Die folgende Syntax ist erfolgreich:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[CONTAINS-Prädikat](-search-sql-contains.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



