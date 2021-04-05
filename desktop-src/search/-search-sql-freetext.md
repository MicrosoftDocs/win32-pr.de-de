---
description: Das Freitext-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Frei Text Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750385"
---
# <a name="freetext-predicate"></a>Frei Text Prädikat

Das Freitext-Prädikat ist Teil der [Where](-search-sql-where.md) -Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten. Verwenden Sie das frei Text Prädikat, um Dokumente zu suchen, die Kombinationen der Suchwörter enthalten, die in den angegebenen Inhalten oder Spalten verteilt sind. Um den Rangwert zu erhalten, schließen Sie "System. search. Rank" ein, bei dem es sich um eine Rangfolge der Relevanz handelt, als eine Spalte in der SELECT-Anweisung.

Das Freitext-Prädikat weist die folgende Syntax auf:


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



Der voll Textspalten Verweis ist optional. Damit können Sie eine einzelne Spalte oder einen [Spalten Gruppierungs Alias](-search-sql-with-as.md) angeben, für den das Freitext Prädikat getestet wird. Wenn die voll Text Spalte als "All" oder "" angegeben wird \* , werden alle indizierten Texteigenschaften durchsucht. Obwohl es sich bei der Spalte nicht um eine Text Eigenschaft handeln muss, können die Ergebnisse bedeutungslos sein, wenn es sich bei der Spalte um einen anderen Datentyp handelt. Der Spaltenname kann entweder ein regulärer oder ein Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen. Wenn keine voll Text Bedingung angegeben wird, wird die Inhaltsspalte verwendet, die den Hauptteil des Dokuments ist.

Sie können ein Suchgebiets Schema angeben, um die entsprechende Wörter Trennung und die Flexions Formen für die Suchabfrage zu identifizieren. Gültige Gebiets Schema Werte sind ein Windows-Standard Sprachcode Bezeichner (LCID). Beispielsweise ist 1033 die LCID für USA-Englisch. Platzieren Sie die LCID als letztes Element innerhalb der Klammern der Freitext-Klausel. Wichtige Informationen zum Suchen von und Sprachen finden [Sie unter Verwenden lokalisierter Such](-search-sql-usinglocsearches.md)Vorgänge.

> [!Note]  
> Das Standard Gebiets Schema für die Suche ist das Standard Gebiets Schema des Systems.

 

Sie müssen den Bereich für die Freitext Bedingung in einfache Anführungszeichen einschließen, und er muss aus mindestens einem Suchbegriff bestehen. Das Freitext Prädikat unterstützt keine logischen Vorgänge. Um nach einem Ausdruck zu suchen, als ob es sich um ein einzelnes Wort handelt, schließen Sie den Ausdruck in doppelte Anführungszeichen ein.

Wenn Sie das frei Text Prädikat verwenden, geben die Suchabfrage Ergebnisse Dokumente zurück, die alle Suchbegriffe enthalten. Die Begriffe müssen nicht in einer bestimmten Reihenfolge angezeigt werden. Dokumente, die mehr Suchbegriffe enthalten, weisen Spaltenwerte höherer Rangfolge auf.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird nach Dokumenten gesucht, die "Computer", "Software", "Hardware" oder Kombinationen aus diesen Wörtern enthalten:


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Es ist nicht möglich, eine einzelne Wort Abgleich und einen übereinstimmenden Ausdruck in demselben Freitext Prädikat zu verwenden.

 

Beim Ausführen von Abfragen mit kontra Zuwendungen müssen Sie das Anführungszeichen bei der Verwendung von frei Text mit Escapezeichen versehen, jedoch nicht, wenn Sie enthält.

Beispielsweise kann die folgende Syntax nicht ausgeführt werden:


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



Die korrekte Syntax umfasst zwei einfache Anführungszeichen, nicht ein doppeltes Anführungszeichen.

Die folgende Syntax ist erfolgreich:


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Enthält Prädikat](-search-sql-contains.md)
</dt> <dt>

[WHERE-Klausel](-search-sql-where.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



