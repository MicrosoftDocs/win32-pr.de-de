---
description: Die im Inhalts Index gespeicherten Spalten können mehrere Werte aufweisen, und diese mehrwertigen Spalten können mithilfe des Array Vergleichs Prädikats verglichen werden.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Mehrwertige Vergleiche (Array)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750376"
---
# <a name="multi-valued-array-comparisons"></a>Mehrwertige Vergleiche (Array)

Die im Inhalts Index gespeicherten Spalten können mehrere Werte aufweisen, und diese mehrwertigen Spalten können mithilfe des Array Vergleichs Prädikats verglichen werden.

Das Array Vergleichs Prädikat weist die folgende Syntax auf:


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



Wenn es sich bei dem Spalten Verweis nicht um eine mehrwertige Spalte handelt, wird ein Fehler zurückgegeben. Der Spaltendatentyp muss mit den Elementen der Vergleichsliste kompatibel sein. Bei Bedarf kann der Spalten [Verweis in einen](-search-sql-castingdatacolumntype.md) anderen Datentyp umgewandelt werden.

Der Vergleichs Operator (Comp \_ OP) kann jeder der normalen Vergleichs Operatoren sein. In einem mehrwertigen Vergleich haben die Vergleichs Operatoren eine etwas andere Bedeutung, je nachdem, ob ein Quantifizierer verwendet wird. Quantifiziererer ermitteln, ob ein Vergleich für alle oder einige der Werte in der Vergleichsliste durchgeführt werden soll. Die Funktionen der Vergleichs Operatoren werden in den Tabellen angegeben, in denen die einzelnen Quantifizierer (All und some) weiter unten in diesem Dokument beschrieben werden.

Der Wert nach dem Operator gibt einen einzelnen Literalwert an, der mit allen Elementen der mehrwertigen Spalte verglichen wird. Wenn ein Element mit dem Wert übereinstimmt, ist das Prädikat "true".

Die Vergleichsliste gibt ein Array von Literalwerten an, die mit der mehrwertigen Spalte verglichen werden. Die Syntax für die Vergleichsliste lautet folgendermaßen:


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> Beachten Sie die Syntax der Vergleichsliste. Die Gruppe von Literalen, die die Vergleichsliste bilden, muss in eckige Klammern eingeschlossen werden. Schließen Sie keine einzelnen Elemente der Vergleichsliste in eckige Klammern ein. Daher sind Array \[ 1 \] und Array \[ 1, 2, 3 \] gültig, array \[ 1 \[ , 2 \] \[ , 3 jedoch \] \] nicht.

 

Die Methode, die verwendet wird, um zu bestimmen, ob der mehrwertige Vergleich true oder false durch den optionalen Quantifizierer zurückgibt. In den folgenden Abschnitten werden die einzelnen Quantifizierer beschrieben und erläutert, wie jeder Vergleichs Operator funktioniert, wenn der Quantifizierer verwendet wird.

## <a name="absent-quantifier"></a>Fehlender Quantifizierer

Wenn kein Quantifizierer angegeben ist, wird jedes Element auf der linken Seite des Vergleichs mit dem Element an derselben Position auf der rechten Seite verglichen. Der Vergleich beginnt mit dem ersten Element in den Arrays und verläuft durch das letzte Element. Wenn alle Elemente auf der linken Seite den entsprechenden Elementen auf der rechten Seite entsprechen, wird die Anzahl der Array Elemente verwendet, um zu bestimmen, welches Array größer ist.

In der folgenden Tabelle wird der Vorgang der Vergleichs Operatoren angezeigt, wenn kein Quantifizierer angegeben ist, und es wird eine kurze Beschreibung der einzelnen Parameter bereitstellt.



| Operator       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Gleich" gibt "true" zurück, wenn jedes Element auf der linken Seite denselben Wert wie das entsprechende Rechte Element hat und beide Arrays die gleiche Anzahl von Elementen aufweisen.                                                                                                                                                                                                                     |
| ! = oder <> | "Ungleich" gibt "true" zurück, wenn ein oder mehrere Elemente auf der linken Seite Werte aufweisen, die sich von den entsprechenden rechtsseitigen Elementen unterscheiden, oder wenn die linksseitigen und rechtsseitigen Arrays nicht die gleiche Anzahl von Elementen aufweisen.                                                                                                                                                              |
| >           | "Größer als" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements größer ist als der Wert des entsprechenden rechtsseitigen Elements. Wenn alle linksseitigen Element Werte genau mit den entsprechenden rechtsseitigen Elementen übereinstimmen und das Array auf der linken Seite mehr Elemente als das Rechte Array aufweist, gibt "größer als" den Wert "true" zurück.                                                     |
| >=          | "Größer als oder gleich" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements größer als oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist. Wenn alle linksseitigen Element Werte gleich oder größer als die entsprechenden rechtsseitigen Elemente sind und das Array auf der linken Seite dieselben oder mehr Elemente als das Rechte Array aufweist, gibt "größer als" true zurück. |
| <           | "Kleiner als" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements kleiner ist als der Wert des entsprechenden rechtsseitigen Elements. "Kleiner als" gibt auch dann "true" zurück, wenn die linke Seite weniger Elemente als die Rechte Seite aufweist.                                                                                                                                                  |
| <=          | "Kleiner als oder gleich" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements kleiner oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist. Wenn alle linksseitigen Element Werte gleich oder kleiner als die entsprechenden rechtsseitigen Elemente sind und das Array auf der linken Seite die gleichen oder weniger Elemente als das Rechte Array aufweist, gibt "größer als" den Wert "true" zurück.         |



 

## <a name="all-quantifier"></a>Sämtlicher Quantifizierer

Der all-Quantifizierer gibt an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird. Um true zurückzugeben, muss der Vergleich für jedes Element auf der linken Seite true sein, wenn es mit jedem Element auf der rechten Seite verglichen wird. Die Anzahl der Elemente in der linken und rechten Array Seite hat keine Auswirkung auf das Ergebnis.

In der folgenden Tabelle wird gezeigt, wie jeder Vergleichs Operator mit dem all-Quantifizierer funktioniert.



| Operator       | BESCHREIBUNG                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Gleich" gibt "true" zurück, wenn jeder Wert auf der linken Seite gleich dem Wert jedes rechtsseitigen Element Werts ist.                              |
| ! = oder <> | "Ungleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte von einem der rechtsseitigen Element Werte abweicht. |
| >           | "Größer als" gibt "true" zurück, wenn jeder linke Elementwert größer als jeder Rechte Elementwert ist.                         |
| >=          | "Größer als oder gleich" gibt "true" zurück, wenn jeder linke Elementwert größer als oder gleich jedem Elementwert rechts ist. |
| <           | "Kleiner als" gibt "true" zurück, wenn jeder linke Elementwert kleiner als jeder Rechte Elementwert ist.                               |
| <=          | "Kleiner als oder gleich" gibt "true" zurück, wenn jeder linke Elementwert kleiner oder gleich jedem Elementwert rechts ist.       |



 

## <a name="some-or-any-quantifier"></a>Ein beliebiger (oder beliebiger) Quantifizierer

Der einige Quantifizierer und der beliebige Quantifizierer können austauschbar verwendet werden. Wie bei allen Quantifizierern gibt der einige Quantifizierer an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird. Um true zurückzugeben, muss der Vergleich für mindestens eines der Elemente auf der linken Seite true sein, wenn es sich um ein beliebiges Element auf der rechten Seite handelt. Die Anzahl der Elemente auf der linken und rechten Seite hat keine Auswirkung auf das Ergebnis.

In der folgenden Tabelle wird gezeigt, wie jeder Vergleichs Operator mit einem bestimmten Quantifizierer funktioniert.



| Operator       | BESCHREIBUNG                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | "Gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte mit einem der rechtsseitigen Element Werte identisch ist.                                  |
| ! = oder <> | "Ungleich" gibt "true" zurück, wenn keine der linksseitigen Element Werte identisch mit den rechten Element Werten ist.                                      |
| >           | "Größer als" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte größer als ein beliebiger rechter Elementwert ist.                         |
| >=          | "Größer als oder gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte größer als oder gleich einem der rechtsseitigen Element Werte ist. |
| <           | "Kleiner als" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte kleiner als ein beliebiger rechter Elementwert ist.                               |
| <=          | "Kleiner als oder gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte kleiner als oder gleich einem der rechtsseitigen Element Werte ist.       |



 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird überprüft, ob Dokumente in den Kategorien "Finanzen" oder "Planung" vorliegen:


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



In den folgenden vergleichen wird true ausgewertet. Beachten Sie, dass die Suchabfrage Syntax tatsächlich erfordert, dass die linke Seite eine Eigenschaft und kein Literalwert ist.


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

[Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[NULL-Prädikat](-search-sql-null.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



