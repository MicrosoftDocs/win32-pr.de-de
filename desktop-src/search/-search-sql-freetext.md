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

Das FREETEXT-Prädikat ist Teil der [WHERE-Klausel](-search-sql-where.md) und unterstützt die Suche nach Wörtern und Ausdrücken in Textspalten. Verwenden Sie das FREETEXT-Prädikat, um Dokumente zu finden, die Kombinationen der Suchwörter enthalten, die über den angegebenen Inhalt oder die angegebenen Spalten verteilt sind. Um den Rangwert zu erhalten, schließen Sie System.Search.Rank, eine Rangfolge der Relevanz, als Spalte in die SELECT-Anweisung ein.

Das FREETEXT-Prädikat hat die folgende Syntax:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



Der Volltextspaltenverweis ist optional. Damit können Sie eine einzelne Spalte [](-search-sql-with-as.md) oder einen Spaltengruppenalias angeben, für den das FREETEXT-Prädikat getestet wird. Wenn die Volltextspalte als "ALL" oder "" angegeben wird, werden alle indizierten \* Texteigenschaften durchsucht. Obwohl die Spalte keine Texteigenschaft sein muss, sind die Ergebnisse möglicherweise bedeutungslos, wenn es sich bei der Spalte um einen anderen Datentyp handelt. Der Spaltenname kann entweder ein regulärer oder ein durch Trennzeichen getrennter [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen. Wenn keine Volltextbedingung angegeben wird, wird die Spalte Inhalt verwendet, bei der es sich um den Text des Dokuments handelt.

Sie können ein Such locale angeben, um die entsprechenden Wörterschalter- und Inflectionalformen für die Suchabfrage zu identifizieren. Gültige Locale-Werte sind ein Windows Standardsprachcodebezeichner (LCID). Beispielsweise ist 1033 die LCID für USA Englisch. Platzieren Sie die LCID als letztes Element in den Klammern der FREETEXT-Klausel. Wichtige Informationen zu Suchen und Sprachen finden Sie unter [Verwenden von lokalisierten Suchvorgängen.](-search-sql-usinglocsearches.md)

> [!Note]  
> Das Standardsuch-Locale ist das Standard-System-Locale.

 

Sie müssen den Freitextbedingungsteil in einfache Anführungszeichen setzen und aus mindestens einem Suchbegriff bestehen. Das FREETEXT-Prädikat unterstützt keine logischen Vorgänge. Um nach einem Ausdruck zu suchen, als wäre es ein einzelnes Wort, schließen Sie ihn in doppelte Anführungszeichen ein.

Wenn Sie das FREETEXT-Prädikat verwenden, geben die Suchergebnisse Dokumente zurück, die alle Suchbegriffe enthalten. Die Begriffe müssen nicht in einer bestimmten Reihenfolge angezeigt werden. Dokumente, die mehr Suchbegriffe enthalten, haben höhere Rangfolgespaltenwerte.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird nach Dokumenten gesucht, die "computer", "software", "hardware" oder Kombinationen dieser Wörter enthalten:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Sie können nicht im gleichen FREETEXT-Prädikat sowohl den Einzelwortabgleich als auch den Ausdrucksabgleich verwenden.

 

Beim Ausführen von Abfragen mit Contractions müssen Sie das Anführungszeichen in der Vertragshürde mit Escapezeichen bei Verwendung von FREETEXT, aber nicht bei Verwendung von CONTAINS escapen.

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

[Nicht-Volltext-Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



