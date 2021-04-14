---
description: Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten aus und gibt einen Wert zurück. Dies ermöglicht es, zusammenfassende Statistiken für Gruppen mit mehreren Ebenen mit geringem mehr Aufwand zu generieren.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Aggregatfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564806"
---
# <a name="aggregate-functions"></a><span data-ttu-id="b2223-104">Aggregatfunktionen</span><span class="sxs-lookup"><span data-stu-id="b2223-104">Aggregate Functions</span></span>

<span data-ttu-id="b2223-105">Eine Aggregatfunktion führt eine Berechnung für einen Satz von Werten aus und gibt einen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="b2223-106">Dies ermöglicht es, zusammenfassende Statistiken für Gruppen mit mehreren Ebenen mit geringem mehr Aufwand zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b2223-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="b2223-107">Informationen zu Aggregatfunktionen</span><span class="sxs-lookup"><span data-stu-id="b2223-107">About Aggregate Functions</span></span>

<span data-ttu-id="b2223-108">Aggregatfunktionen in Windows Search Structured Query Language (SQL) weisen die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="b2223-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="b2223-109">Der Funktionsteil kann eine der folgenden Funktionen und Syntax einschließen:</span><span class="sxs-lookup"><span data-stu-id="b2223-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="b2223-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="b2223-110">Function</span></span>                                                              | <span data-ttu-id="b2223-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2223-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2223-112">AVG ( <column> )</span><span class="sxs-lookup"><span data-stu-id="b2223-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="b2223-113">Gibt den Mittelwert der Werte in einer Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="b2223-114">Gilt nur für Zahlen.</span><span class="sxs-lookup"><span data-stu-id="b2223-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="b2223-115">Byfrequency ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="b2223-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="b2223-116">Gibt die häufigsten N Spaltenwerte aus den Ergebnissen in der Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="b2223-117">Umfasst außerdem die Anzahl der Vorkommen der einzelnen Werte und Dokument Bezeichner für Ergebnisse, die jeden zurückgegebenen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="b2223-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="b2223-118">ChildCount ()</span><span class="sxs-lookup"><span data-stu-id="b2223-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="b2223-119">Gibt die Anzahl der Elemente in einer Gruppe zurück (ausgenommen Untergruppen).</span><span class="sxs-lookup"><span data-stu-id="b2223-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="b2223-120">Wenn mehrere Gruppierungs Ebenen vorhanden sind, wird die Anzahl der unmittelbaren untergeordneten Gruppen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2223-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="b2223-121">COUNT ()</span><span class="sxs-lookup"><span data-stu-id="b2223-121">COUNT()</span></span>                                                               | <span data-ttu-id="b2223-122">Gibt die Anzahl der Elemente in einer Gruppe und alle Untergruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="b2223-123">DateRange ( <column> )</span><span class="sxs-lookup"><span data-stu-id="b2223-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="b2223-124">Gibt die unteren und oberen Begrenzungen der Spaltenwerte zurück, die in der Gruppen Ergebnis Gruppe gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="b2223-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="b2223-125">Gilt nur für FILETIME-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2223-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="b2223-126">First ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="b2223-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="b2223-127">Gibt die ersten N Spaltenwerte aus den in einer Gruppe gefundenen Blatt Ergebnissen zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="b2223-128">Max ( <column> )</span><span class="sxs-lookup"><span data-stu-id="b2223-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="b2223-129">Gibt den größten Wert im Ausdruck zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="b2223-130">Gilt nur für Zahlen oder Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="b2223-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="b2223-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="b2223-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="b2223-132">Gibt den kleinsten Wert im Ausdruck zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="b2223-133">Gilt nur für Zahlen oder Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="b2223-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="b2223-134">Representativeof ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="b2223-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="b2223-135">Gibt N idrepresentative-Werte zurück, die jeweils aus einer der Ergebnis Teilmengen mit einem eindeutigen Spaltenwert ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="b2223-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="b2223-136">Jeder Wert wird auch mit einem Dokument Bezeichner mit dem idrepresentative-Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2223-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="b2223-137">Sum ( <column> )</span><span class="sxs-lookup"><span data-stu-id="b2223-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="b2223-138">Gibt die Summe der Werte in einer Gruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="b2223-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="b2223-139">Gilt nur für Zahlen.</span><span class="sxs-lookup"><span data-stu-id="b2223-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="b2223-140">Aggregate werden als einzelne Spalten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2223-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="b2223-141">Sie sind größtenteils einfache Typen mit Ausnahme von byfrequency, First, DateRange und representativeof, die als Verbund Typen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2223-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="b2223-142">Sie können eine beliebige numerische oder Datums Spalte für Aggregationen verwenden, und nicht nur diejenigen, die in der SELECT-Klausel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b2223-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="b2223-143">Sie können jedoch keine Gruppierung von Aggregaten durchführt.</span><span class="sxs-lookup"><span data-stu-id="b2223-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="b2223-144">Ein Syntax Fehler wird zurückgegeben, wenn das über gegebene Spalten Argument weder ein numerischer noch ein Date-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="b2223-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="b2223-145">Der Bezeichnungs Teil ist optional und bietet einen besser lesbaren Alias für die Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="b2223-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="b2223-146">Wenn Sie keine Alias Bezeichnung einschließen, transformiert Windows Search den Funktions-und Spaltennamen in eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="b2223-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="b2223-147">Beispiel: Max (System.DocAnzahl. WordCount) wird zu Max \_ systemdocumentwordcount.</span><span class="sxs-lookup"><span data-stu-id="b2223-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="b2223-148">Gruppen und zählen auf mehreren Ebenen</span><span class="sxs-lookup"><span data-stu-id="b2223-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="b2223-149">Aggregate werden über Blätter definiert und dupliziert.</span><span class="sxs-lookup"><span data-stu-id="b2223-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="b2223-150">Ein Aggregat übernimmt als Eingabe die Blätter der Gruppe, die es definiert (Dokumente), anstatt die untergeordneten Gruppen seiner untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="b2223-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="b2223-151">Diese Funktion wird als Gruppierung mit mehreren Ebenen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b2223-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="b2223-152">Zusätzlich zu den Aggregaten, die über Blätter definiert und dupliziert werden, werden Sie nur einmal gezählt.</span><span class="sxs-lookup"><span data-stu-id="b2223-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="b2223-153">Obwohl das gleiche Dokument mehrmals unter einer Gruppe dargestellt werden kann, wird es von Aggregaten nur einmal berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b2223-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="b2223-154">Dieses Konzept wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b2223-154">The following graphic illustrates this concept.</span></span>

![Diagramm, das anzeigt, dass Aggregate über Blätter definiert und dupliziert werden und nur einmal gezählt werden](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="b2223-156">Aggregat Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2223-156">Aggregate Examples</span></span>

<span data-ttu-id="b2223-157">Im folgenden finden Sie Beispiele für Aggregatfunktionen innerhalb der Group on-Klausel:</span><span class="sxs-lookup"><span data-stu-id="b2223-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="b2223-158">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2223-158">Return Value</span></span>

<span data-ttu-id="b2223-159">Der Rückgabewert ist eine Variante, die im Rowset als benutzerdefinierte Eigenschaft gefunden wird, entweder als angegebene Aliase oder als "Aggregate", wenn keine Alias Bezeichnung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b2223-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



