---
description: Spaltengruppenaliase bieten eine Möglichkeit, kürzere Namen anstelle des Namens einer Spalte oder einer Gruppe von Spalten zu verwenden. Das optionale Gruppenaliasprädikat ist Teil der WHERE-Klausel.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH – AS-Gruppenaliasprädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226733"
---
# <a name="with----as-group-alias-predicate"></a>WITH – AS-Gruppenaliasprädikat

Spaltengruppenaliase bieten eine Möglichkeit, kürzere Namen anstelle des Namens einer Spalte oder einer Gruppe von Spalten zu verwenden. Das optionale Gruppenaliasprädikat ist Teil der WHERE-Klausel. Die Syntax lautet wie folgt:


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



Sie können mehrere Gruppenaliase angeben, wobei Sie with... AS-Prädikate durch Kommas.

Wenn in einem WHERE-Klauselprädikat auf einen Gruppenalias verwiesen wird, wird die Bedingung auf jede Spalte in der Gruppe angewendet. Die logischen Werte, die sich aus dem Abgleich der einzelnen Spalten ergeben, werden mithilfe des logischen **OR-Operators** kombiniert.

Ein Alias muss definiert werden, bevor er verwendet werden kann, und er kann nur innerhalb der WHERE-Klausel verwendet werden. Der Aliasname muss ein regulärer Bezeichner sein, dem ein erforderliches Nummernzeichen ( ) vorangestellt \# ist.

Der Spaltenspezifizierer kann einen oder mehrere Spaltenspezifizierer enthalten, die durch Kommas getrennt sind. Die Liste der Spalten muss in Klammern eingeschlossen werden, und jeder Spalte kann eine Gewichtung zugewiesen werden. Jede Spalte weist die folgende Syntax auf:


```
<column_identifier> [<weight_assignment>]
```



Informationen zum Angeben von Spaltengewichtungen finden Sie unter [FREETEXT-Prädikat](-search-sql-freetext.md) und [CONTAINS-Prädikat.](-search-sql-contains.md)

Der Spaltenbezeichner kann normal oder durch Trennzeichen getrennt sein.

## <a name="examples"></a>Beispiele

Die folgenden WHERE-Klauselbeispiele veranschaulichen, wann und wie Sie das Gruppenaliasprädikat verwenden können. Das erste Beispiel zeigt eine sich wiederholende WHERE-Klausel, die kein Gruppenaliasing verwendet.


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



Im Folgenden ist ein Beispiel für eine positive Gewichtung angegeben, bei der die **Title-Eigenschaft** bei der Bestimmung des relativen Rangs eine größere Gewichtung erhält.


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



Es folgt ein Beispiel für eine negative Gewichtung, bei der die **Title-Eigenschaft** mit der Gewichtung 0 nicht berücksichtigt wird.


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

[FREETEXT-Prädikat](-search-sql-freetext.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



