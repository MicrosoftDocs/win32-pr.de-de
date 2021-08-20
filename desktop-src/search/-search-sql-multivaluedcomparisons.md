---
description: Im Inhaltsindex gespeicherte Spalten können mehrere Werte enthalten, und diese mehrwertigen Spalten können mit dem ARRAY-Vergleichs prädikat verglichen werden.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Mehrwertige Vergleiche (ARRAY)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043ed6744717ac3156d9dd64f2f6806f2ffc509107f5bcdc8a66980e5cdd0012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863369"
---
# <a name="multi-valued-array-comparisons"></a>Mehrwertige Vergleiche (ARRAY)

Im Inhaltsindex gespeicherte Spalten können mehrere Werte enthalten, und diese mehrwertigen Spalten können mit dem ARRAY-Vergleichs prädikat verglichen werden.

Das ARRAY-Vergleichs prädikat hat die folgende Syntax:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Wenn der Spaltenverweis keine mehrwertige Spalte ist, wird ein Fehler zurückgegeben. Der Spaltendatentyp muss mit den Elementen der Vergleichsliste kompatibel sein. Bei Bedarf kann der Spaltenverweis in [einen anderen](-search-sql-castingdatacolumntype.md) Datentyp cast werden.

Der Vergleichsoperator (comp \_ op) kann einer der normalen Vergleichsoperatoren sein. In einem mehrwertigen Vergleich haben die Vergleichsoperatoren geringfügig unterschiedliche Bedeutungen, je nachdem, ob ein Quantifizierer verwendet wird. Quantifizierer bestimmen, ob ein Vergleich mit allen oder einigen der Werte in der Vergleichsliste vorgenommen werden soll. Die Funktionen der Vergleichsoperatoren werden in den Tabellen angegeben, in denen die einzelnen Quantifizierer (ALL und SOME) weiter später in diesem Dokument beschrieben werden.

Der Wert nach dem Operator gibt einen einzelnen Literalwert an, der mit allen Elementen der mehrwertigen Spalte verglichen wird. Wenn ein Element dem Wert entspricht, ist das Prädikat true.

Die Vergleichsliste gibt ein Array von Literalwerten an, die mit der mehrwertigen Spalte verglichen werden. Die Syntax für die Vergleichsliste lautet wie folgt:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Beachten Sie die Syntax der Vergleichsliste. Die Gruppe von Literalen, aus denen die Vergleichsliste erstellt wird, muss in eckige Klammern eingeschlossen werden. Umschließen Sie einzelne Elemente der Vergleichsliste nicht in eckige Klammern. Daher sind ARRAY \[ 1 \] und ARRAY \[ 1,2,3 \] gültig, ARRAY \[ 1 \[ ,2 \] \[ ,3 jedoch \] \] nicht.

 

Die Methode, mit der bestimmt wird, ob der mehrwertige Vergleich TRUE oder FALSE zurückgibt, wird vom optionalen Quantifizierer angegeben. In den folgenden Abschnitten werden die einzelnen Quantifizierer und die Funktionsweise der einzelnen Vergleichsoperator beschrieben, wenn der Quantifizierer verwendet wird.

## <a name="absent-quantifier"></a>Absent Quantifier

Wenn kein Quantifizierer angegeben wird, wird jedes Element auf der linken Seite des Vergleichs mit dem Element an der gleichen Position auf der rechten Seite verglichen. Der Vergleich beginnt mit dem ersten Element in den Arrays und durchschreitet das letzte Element. Wenn alle Elemente auf der linken Seite den entsprechenden Elementen auf der rechten Seite entsprechen, wird die Anzahl der Arrayelemente verwendet, um zu bestimmen, welches Array größer ist.

Die folgende Tabelle zeigt die Operation der Vergleichsoperatoren, wenn kein Quantifizierer angegeben ist, und bietet eine kurze Beschreibung der einzelnen Operatoren.



| Operator       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Equal to" gibt TRUE zurück, wenn jedes linke Element den gleichen Wert wie das entsprechende rechte Element hat und beide Arrays die gleiche Anzahl von Elementen haben.                                                                                                                                                                                                                     |
| != oder <> | "Not equal to" gibt TRUE zurück, wenn ein oder mehrere linksseitige Elemente Werte haben, die sich von den entsprechenden rechten Elementen unterscheiden, oder wenn das linke und das rechte Array nicht die gleiche Anzahl von Elementen haben.                                                                                                                                                              |
| >           | "Größer als" gibt TRUE zurück, wenn der Wert jedes linken Elements größer als der Wert des entsprechenden rechtsseitigen Elements ist. Wenn alle werte des linken Elements genau mit den entsprechenden rechten Elementen übereinstimmen und das linke Array über mehr Elemente als das rechte Array verfügt, gibt "größer als" true zurück.                                                     |
| >=          | "Größer als oder gleich" gibt TRUE zurück, wenn der Wert jedes linken Elements größer oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist. Wenn alle Linken-Elementwerte gleich oder größer als die entsprechenden rechtsseitigen Elemente sind und das linke Array die gleichen oder mehr Elemente wie das rechte Array hat, gibt "größer als" TRUE zurück. |
| <           | "Less than" gibt TRUE zurück, wenn der Wert jedes linken Elements kleiner als der Wert des entsprechenden rechtsseitigen Elements ist. "Kleiner als" gibt auch TRUE zurück, wenn die linke Seite weniger Elemente als die rechte Seite hat.                                                                                                                                                  |
| <=          | "Kleiner als oder gleich" gibt TRUE zurück, wenn der Wert jedes linken Elements kleiner oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist. Wenn alle linken Elementwerte gleich oder kleiner als die entsprechenden rechtsseitigen Elemente sind und das linke Array über die gleichen oder weniger Elemente als das rechte Array verfügt, gibt "größer als" TRUE zurück.         |



 

## <a name="all-quantifier"></a>ALL Quantifier

Der ALL-Quantifizierer gibt an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird. Um TRUE zurück zu geben, muss der Vergleich für jedes Element auf der linken Seite true sein, wenn er mit jedem Element auf der rechten Seite verglichen wird. Die Anzahl der Elemente auf der linken und rechten Arrayseite hat keine Auswirkungen auf das Ergebnis.

Die folgende Tabelle zeigt, wie jeder Vergleichsoperator mit dem ALL-Quantifizierer funktioniert.



| Operator       | Beschreibung                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Equal to" gibt TRUE zurück, wenn jeder linke Elementwert mit jedem rechten Elementwert identisch ist.                              |
| != oder <> | "Not equal to" gibt TRUE zurück, wenn sich mindestens einer der linken Elementwerte von einem der rechten Elementwerte unterscheiden. |
| >           | "Größer als" gibt TRUE zurück, wenn jeder linke Elementwert größer als jeder rechte Elementwert ist.                         |
| >=          | "Größer als oder gleich" gibt TRUE zurück, wenn jeder linke Elementwert größer oder gleich jedem rechten Elementwert ist. |
| <           | "Kleiner als" gibt TRUE zurück, wenn jeder linke Elementwert kleiner als jeder rechte Elementwert ist.                               |
| <=          | "Kleiner als oder gleich" gibt TRUE zurück, wenn jeder linke Elementwert kleiner oder gleich jedem rechten Elementwert ist.       |



 

## <a name="some-or-any-quantifier"></a>SOME-Quantifizierer (oder ANY-Quantifizierer)

Der SOME-Quantifizierer und der ANY-Quantifizierer können austauschbar verwendet werden. Wie der ALL-Quantifizierer gibt der SOME-Quantifizierer an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird. Um TRUE zurück zu geben, muss der Vergleich für mindestens eines der Elemente auf der linken Seite true sein, wenn er mit einem element auf der rechten Seite verglichen wird. Die Anzahl der Elemente auf dem linken und rechten Array hat keine Auswirkungen auf das Ergebnis.

Die folgende Tabelle zeigt, wie jeder Vergleichsoperator mit dem SOME-Quantifizierer funktioniert.



| Operator       | Beschreibung                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Equal to" gibt TRUE zurück, wenn mindestens einer der linken Elementwerte mit einem der werte des rechten Elements identisch ist.                                  |
| != oder <> | "Not equal to" gibt TRUE zurück, wenn keiner der linken Elementwerte mit einem der werte des rechten Elements identisch ist.                                      |
| >           | "Größer als" gibt TRUE zurück, wenn mindestens einer der linken Elementwerte größer als einer der werte des rechten Elements ist.                         |
| >=          | "Größer als oder gleich" gibt TRUE zurück, wenn mindestens einer der linken Elementwerte größer oder gleich einem der werte des rechten Elements ist. |
| <           | "Less than" gibt TRUE zurück, wenn mindestens einer der linken Elementwerte kleiner als einer der werte des rechten Elements ist.                               |
| <=          | "Kleiner als oder gleich" gibt TRUE zurück, wenn mindestens einer der linken Elementwerte kleiner oder gleich einem der werte des rechten Elements ist.       |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird überprüft, ob Dokumente in den Kategorien "Finanzen" oder "Planung" enthalten sind:


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



Die folgenden Vergleiche werden alle als "true" ausgewertet. Beachten Sie, dass die Syntax der Suchabfrage bei der tatsächlichen Verwendung erfordert, dass die linke Seite eine Eigenschaft und kein Literalwert ist.


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[LIKE-Prädikat](-search-sql-like.md)
</dt> <dt>

[Literalwertvergleich](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[NULL-Prädikat](-search-sql-null.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltext-Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltext-Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



