---
description: Spalten Gruppen Aliase bieten eine Möglichkeit, kürzere Namen anstelle des Namens einer Spalte oder einer Gruppe von Spalten zu verwenden. Das optionale Gruppenalias-Prädikat ist Teil der WHERE-Klausel.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH--as Group Alias-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750368"
---
# <a name="with----as-group-alias-predicate"></a>WITH--as Group Alias-Prädikat

Spalten Gruppen Aliase bieten eine Möglichkeit, kürzere Namen anstelle des Namens einer Spalte oder einer Gruppe von Spalten zu verwenden. Das optionale Gruppenalias-Prädikat ist Teil der WHERE-Klausel. Die Syntax folgt:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Sie können mehr als einen Gruppenalias angeben, indem Sie den durch... Als Prädikate durch Kommas.

Wenn in einem WHERE-Klausel-Prädikat auf einen gruppeneralias verwiesen wird, wird die Bedingung auf jede Spalte in der Gruppe angewendet. Die logischen Werte, die sich aus der Übereinstimmung der einzelnen Spalten ergeben, werden mithilfe des logischen **or** -Operators kombiniert.

Ein Alias muss definiert werden, bevor er verwendet werden kann, und er kann nur innerhalb der WHERE-Klausel verwendet werden. Der Aliasname muss ein regulärer Bezeichner sein, dem ein erforderliches Nummern Zeichen () vorangestellt ist \# .

Der Spalten Bezeichner kann einen oder mehrere Spalten Spezifizierer enthalten, die durch Kommas getrennt sind. Die Liste der Spalten muss in Klammern eingeschlossen werden, und jeder kann eine Gewichtung zugewiesen werden. Jede Spalte weist die folgende Syntax auf:


```
<column_identifier> [<weight_assignment>]
```



Weitere Informationen zum Angeben von Spalten Gewichtungen finden Sie unter frei [Text Prädikat](-search-sql-freetext.md) und [enthält Prädikat](-search-sql-contains.md).

Der Spalten Bezeichner kann regulär oder getrennt sein.

## <a name="examples"></a>Beispiele

Die folgenden WHERE-klauselbeispiele veranschaulichen, wann und wie Sie das Gruppenalias Prädikat verwenden können. Das erste Beispiel zeigt eine immer wiederkehrende WHERE-Klausel, die keine Gruppen Aliasing verwendet.


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



Das vorherige Beispiel kann mithilfe eines Gruppenalias vereinfacht werden, wie im folgenden Beispiel gezeigt.


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Im folgenden finden Sie ein Beispiel für eine positive Gewichtung, bei der die **Title** -Eigenschaft bei der Bestimmung des relativen Rangs stärker gewichtet wird.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Im folgenden finden Sie ein Beispiel für eine negative Gewichtung, bei der die **Title** -Eigenschaft mit Gewichtung von 0 nicht berücksichtigt wird.


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Frei Text Prädikat](-search-sql-freetext.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



