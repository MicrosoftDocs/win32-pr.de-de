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
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="7ac56-103">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="7ac56-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="7ac56-104">Die im Inhalts Index gespeicherten Spalten können mehrere Werte aufweisen, und diese mehrwertigen Spalten können mithilfe des Array Vergleichs Prädikats verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="7ac56-105">Das Array Vergleichs Prädikat weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="7ac56-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="7ac56-106">Wenn es sich bei dem Spalten Verweis nicht um eine mehrwertige Spalte handelt, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ac56-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="7ac56-107">Der Spaltendatentyp muss mit den Elementen der Vergleichsliste kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="7ac56-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="7ac56-108">Bei Bedarf kann der Spalten [Verweis in einen](-search-sql-castingdatacolumntype.md) anderen Datentyp umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="7ac56-109">Der Vergleichs Operator (Comp \_ OP) kann jeder der normalen Vergleichs Operatoren sein.</span><span class="sxs-lookup"><span data-stu-id="7ac56-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="7ac56-110">In einem mehrwertigen Vergleich haben die Vergleichs Operatoren eine etwas andere Bedeutung, je nachdem, ob ein Quantifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="7ac56-111">Quantifiziererer ermitteln, ob ein Vergleich für alle oder einige der Werte in der Vergleichsliste durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ac56-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="7ac56-112">Die Funktionen der Vergleichs Operatoren werden in den Tabellen angegeben, in denen die einzelnen Quantifizierer (All und some) weiter unten in diesem Dokument beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="7ac56-113">Der Wert nach dem Operator gibt einen einzelnen Literalwert an, der mit allen Elementen der mehrwertigen Spalte verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="7ac56-114">Wenn ein Element mit dem Wert übereinstimmt, ist das Prädikat "true".</span><span class="sxs-lookup"><span data-stu-id="7ac56-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="7ac56-115">Die Vergleichsliste gibt ein Array von Literalwerten an, die mit der mehrwertigen Spalte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="7ac56-116">Die Syntax für die Vergleichsliste lautet folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="7ac56-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="7ac56-117">Beachten Sie die Syntax der Vergleichsliste.</span><span class="sxs-lookup"><span data-stu-id="7ac56-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="7ac56-118">Die Gruppe von Literalen, die die Vergleichsliste bilden, muss in eckige Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="7ac56-119">Schließen Sie keine einzelnen Elemente der Vergleichsliste in eckige Klammern ein.</span><span class="sxs-lookup"><span data-stu-id="7ac56-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="7ac56-120">Daher sind Array \[ 1 \] und Array \[ 1, 2, 3 \] gültig, array \[ 1 \[ , 2 \] \[ , 3 jedoch \] \] nicht.</span><span class="sxs-lookup"><span data-stu-id="7ac56-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="7ac56-121">Die Methode, die verwendet wird, um zu bestimmen, ob der mehrwertige Vergleich true oder false durch den optionalen Quantifizierer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7ac56-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="7ac56-122">In den folgenden Abschnitten werden die einzelnen Quantifizierer beschrieben und erläutert, wie jeder Vergleichs Operator funktioniert, wenn der Quantifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="7ac56-123">Fehlender Quantifizierer</span><span class="sxs-lookup"><span data-stu-id="7ac56-123">Absent Quantifier</span></span>

<span data-ttu-id="7ac56-124">Wenn kein Quantifizierer angegeben ist, wird jedes Element auf der linken Seite des Vergleichs mit dem Element an derselben Position auf der rechten Seite verglichen.</span><span class="sxs-lookup"><span data-stu-id="7ac56-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="7ac56-125">Der Vergleich beginnt mit dem ersten Element in den Arrays und verläuft durch das letzte Element.</span><span class="sxs-lookup"><span data-stu-id="7ac56-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="7ac56-126">Wenn alle Elemente auf der linken Seite den entsprechenden Elementen auf der rechten Seite entsprechen, wird die Anzahl der Array Elemente verwendet, um zu bestimmen, welches Array größer ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="7ac56-127">In der folgenden Tabelle wird der Vorgang der Vergleichs Operatoren angezeigt, wenn kein Quantifizierer angegeben ist, und es wird eine kurze Beschreibung der einzelnen Parameter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7ac56-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="7ac56-128">Operator</span><span class="sxs-lookup"><span data-stu-id="7ac56-128">Operator</span></span>       | <span data-ttu-id="7ac56-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ac56-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7ac56-130">"Gleich" gibt "true" zurück, wenn jedes Element auf der linken Seite denselben Wert wie das entsprechende Rechte Element hat und beide Arrays die gleiche Anzahl von Elementen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7ac56-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="7ac56-131">! = oder <></span><span class="sxs-lookup"><span data-stu-id="7ac56-131">!= or <></span></span> | <span data-ttu-id="7ac56-132">"Ungleich" gibt "true" zurück, wenn ein oder mehrere Elemente auf der linken Seite Werte aufweisen, die sich von den entsprechenden rechtsseitigen Elementen unterscheiden, oder wenn die linksseitigen und rechtsseitigen Arrays nicht die gleiche Anzahl von Elementen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7ac56-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="7ac56-133">"Größer als" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements größer ist als der Wert des entsprechenden rechtsseitigen Elements.</span><span class="sxs-lookup"><span data-stu-id="7ac56-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="7ac56-134">Wenn alle linksseitigen Element Werte genau mit den entsprechenden rechtsseitigen Elementen übereinstimmen und das Array auf der linken Seite mehr Elemente als das Rechte Array aufweist, gibt "größer als" den Wert "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="7ac56-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="7ac56-135">"Größer als oder gleich" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements größer als oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="7ac56-136">Wenn alle linksseitigen Element Werte gleich oder größer als die entsprechenden rechtsseitigen Elemente sind und das Array auf der linken Seite dieselben oder mehr Elemente als das Rechte Array aufweist, gibt "größer als" true zurück.</span><span class="sxs-lookup"><span data-stu-id="7ac56-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="7ac56-137">"Kleiner als" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements kleiner ist als der Wert des entsprechenden rechtsseitigen Elements.</span><span class="sxs-lookup"><span data-stu-id="7ac56-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="7ac56-138">"Kleiner als" gibt auch dann "true" zurück, wenn die linke Seite weniger Elemente als die Rechte Seite aufweist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="7ac56-139">"Kleiner als oder gleich" gibt "true" zurück, wenn der Wert jedes linksseitigen Elements kleiner oder gleich dem Wert des entsprechenden rechtsseitigen Elements ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="7ac56-140">Wenn alle linksseitigen Element Werte gleich oder kleiner als die entsprechenden rechtsseitigen Elemente sind und das Array auf der linken Seite die gleichen oder weniger Elemente als das Rechte Array aufweist, gibt "größer als" den Wert "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="7ac56-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="7ac56-141">Sämtlicher Quantifizierer</span><span class="sxs-lookup"><span data-stu-id="7ac56-141">ALL Quantifier</span></span>

<span data-ttu-id="7ac56-142">Der all-Quantifizierer gibt an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="7ac56-143">Um true zurückzugeben, muss der Vergleich für jedes Element auf der linken Seite true sein, wenn es mit jedem Element auf der rechten Seite verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="7ac56-144">Die Anzahl der Elemente in der linken und rechten Array Seite hat keine Auswirkung auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="7ac56-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="7ac56-145">In der folgenden Tabelle wird gezeigt, wie jeder Vergleichs Operator mit dem all-Quantifizierer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7ac56-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="7ac56-146">Operator</span><span class="sxs-lookup"><span data-stu-id="7ac56-146">Operator</span></span>       | <span data-ttu-id="7ac56-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ac56-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7ac56-148">"Gleich" gibt "true" zurück, wenn jeder Wert auf der linken Seite gleich dem Wert jedes rechtsseitigen Element Werts ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="7ac56-149">! = oder <></span><span class="sxs-lookup"><span data-stu-id="7ac56-149">!= or <></span></span> | <span data-ttu-id="7ac56-150">"Ungleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte von einem der rechtsseitigen Element Werte abweicht.</span><span class="sxs-lookup"><span data-stu-id="7ac56-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="7ac56-151">"Größer als" gibt "true" zurück, wenn jeder linke Elementwert größer als jeder Rechte Elementwert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="7ac56-152">"Größer als oder gleich" gibt "true" zurück, wenn jeder linke Elementwert größer als oder gleich jedem Elementwert rechts ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="7ac56-153">"Kleiner als" gibt "true" zurück, wenn jeder linke Elementwert kleiner als jeder Rechte Elementwert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="7ac56-154">"Kleiner als oder gleich" gibt "true" zurück, wenn jeder linke Elementwert kleiner oder gleich jedem Elementwert rechts ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="7ac56-155">Ein beliebiger (oder beliebiger) Quantifizierer</span><span class="sxs-lookup"><span data-stu-id="7ac56-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="7ac56-156">Der einige Quantifizierer und der beliebige Quantifizierer können austauschbar verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ac56-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="7ac56-157">Wie bei allen Quantifizierern gibt der einige Quantifizierer an, dass jedes Element auf der linken Seite mit jedem Element auf der rechten Seite verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="7ac56-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="7ac56-158">Um true zurückzugeben, muss der Vergleich für mindestens eines der Elemente auf der linken Seite true sein, wenn es sich um ein beliebiges Element auf der rechten Seite handelt.</span><span class="sxs-lookup"><span data-stu-id="7ac56-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="7ac56-159">Die Anzahl der Elemente auf der linken und rechten Seite hat keine Auswirkung auf das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="7ac56-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="7ac56-160">In der folgenden Tabelle wird gezeigt, wie jeder Vergleichs Operator mit einem bestimmten Quantifizierer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7ac56-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="7ac56-161">Operator</span><span class="sxs-lookup"><span data-stu-id="7ac56-161">Operator</span></span>       | <span data-ttu-id="7ac56-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ac56-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="7ac56-163">"Gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte mit einem der rechtsseitigen Element Werte identisch ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="7ac56-164">! = oder <></span><span class="sxs-lookup"><span data-stu-id="7ac56-164">!= or <></span></span> | <span data-ttu-id="7ac56-165">"Ungleich" gibt "true" zurück, wenn keine der linksseitigen Element Werte identisch mit den rechten Element Werten ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="7ac56-166">"Größer als" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte größer als ein beliebiger rechter Elementwert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="7ac56-167">"Größer als oder gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte größer als oder gleich einem der rechtsseitigen Element Werte ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="7ac56-168">"Kleiner als" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte kleiner als ein beliebiger rechter Elementwert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="7ac56-169">"Kleiner als oder gleich" gibt "true" zurück, wenn mindestens einer der linksseitigen Element Werte kleiner als oder gleich einem der rechtsseitigen Element Werte ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="7ac56-170">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ac56-170">Examples</span></span>

<span data-ttu-id="7ac56-171">Im folgenden Beispiel wird überprüft, ob Dokumente in den Kategorien "Finanzen" oder "Planung" vorliegen:</span><span class="sxs-lookup"><span data-stu-id="7ac56-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="7ac56-172">In den folgenden vergleichen wird true ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="7ac56-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="7ac56-173">Beachten Sie, dass die Suchabfrage Syntax tatsächlich erfordert, dass die linke Seite eine Eigenschaft und kein Literalwert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac56-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="7ac56-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ac56-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7ac56-175">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="7ac56-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ac56-176">LIKE-Prädikat</span><span class="sxs-lookup"><span data-stu-id="7ac56-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="7ac56-177">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="7ac56-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="7ac56-178">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="7ac56-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="7ac56-179">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7ac56-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7ac56-180">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="7ac56-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="7ac56-181">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="7ac56-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



