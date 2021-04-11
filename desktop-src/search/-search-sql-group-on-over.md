---
description: Die Gruppe in...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: Gruppieren nach... Über... An
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128541"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="4060c-103">Gruppieren nach... Über... An</span><span class="sxs-lookup"><span data-stu-id="4060c-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="4060c-104">Die Gruppe in... Über... die-Anweisung gibt ein hierarchisches Rowset zurück, in dem Suchergebnisse auf der Grundlage einer angegebenen Spalte und optionaler Gruppierungs Bereiche in Gruppen aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="4060c-105">Wenn Sie in der Spalte [System. Kind](../properties/props-system-kind.md) gruppieren, ist das Resultset in mehrere Gruppen unterteilt: eine für Dokumente, eine für die Kommunikation usw.</span><span class="sxs-lookup"><span data-stu-id="4060c-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="4060c-106">Wenn Sie [System. Size](../properties/props-system-size.md) und den Gruppenbereich 100 KB gruppieren, ist das Resultset in drei Gruppen unterteilt: Elemente der Größe < 100 KB, Elemente der Größe >= 100 KB und Elemente ohne Größen Wert.</span><span class="sxs-lookup"><span data-stu-id="4060c-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="4060c-107">Sie können auch Gruppierungen mit Funktionen aggregieren.</span><span class="sxs-lookup"><span data-stu-id="4060c-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="4060c-108">In diesem Thema werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="4060c-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="4060c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4060c-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="4060c-110">Gruppen Bereiche</span><span class="sxs-lookup"><span data-stu-id="4060c-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="4060c-111">Bezeichnen von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="4060c-112">Anordnen von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="4060c-113">Schachteln von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="4060c-114">Gruppieren von Vektor Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4060c-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="4060c-115">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="4060c-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="4060c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4060c-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="4060c-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="4060c-117">Syntax</span></span>

<span data-ttu-id="4060c-118">Die Gruppe in... Über... die-Anweisung weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="4060c-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="4060c-119">Dabei werden Gruppierungs Bereiche wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4060c-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="4060c-120">Die Gruppe in <column> kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md) für eine Eigenschaft im Eigenschaften Speicher sein.</span><span class="sxs-lookup"><span data-stu-id="4060c-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="4060c-121">Der optionale <group ranges> ist eine Liste mit einem oder mehreren Werten (Anzahl, Datum oder Zeichenfolge), die zum Aufteilen der Ergebnisse in Gruppen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="4060c-122">Der <range limit> identifiziert einen Divisions Punkt im zurückgegebenen Resultset, und der <label> identifiziert eine benutzerfreundliche Bezeichnung für eine Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4060c-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="4060c-123">Sie können das Resultset in beliebig viele Gruppen aufteilen.</span><span class="sxs-lookup"><span data-stu-id="4060c-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="4060c-124">Die erste Gruppe der Ergebnisse umfasst Elemente mit dem minimal möglichen Wert für die angegebene Eigenschaft bis zum ersten Bereichs Limit.</span><span class="sxs-lookup"><span data-stu-id="4060c-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="4060c-125">Auf diese Gruppe kann mit dem MinValue-Schlüsselwort verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="4060c-126">Auf die zweite Gruppe kann mit dem bereichsbeschränkungsspezifizierer selbst verwiesen werden. Sie enthält Elemente, deren Wert für die angegebene Eigenschaft größer oder gleich dem Bereichs Limit ist.</span><span class="sxs-lookup"><span data-stu-id="4060c-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="4060c-127">Alle Elemente, die nicht über einen Wert für die angegebene Eigenschaft verfügen, werden zuletzt zurückgegeben, und auf Sie kann mit dem **null** -Schlüsselwort verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="4060c-128">Beispielsweise dividiert eine Bereichs Beschränkung von "2006-01-01" für die [System. DateCreated](../properties/props-system-datecreated.md) -Eigenschaft das Resultset in Elemente mit Datumsangaben vor 2006-01-01 (MinValue-Gruppe), Elementen mit Datumsangaben auf oder nach 2006-01-01 (2006-01-01-Gruppe) und Elementen ohne Datum (**null** -Gruppe).</span><span class="sxs-lookup"><span data-stu-id="4060c-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="4060c-129">In jeder Gruppe werden die Ergebnisse standardmäßig nach den Werten in der Spalte Gruppieren nach sortiert.</span><span class="sxs-lookup"><span data-stu-id="4060c-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="4060c-130">Die optionale [Order by](-search-sql-orderby.md) -Klausel kann einen Zugriffsspezifizierer von ASC für aufsteigend (niedrig zu hoch) oder für absteigend (hoch bis niedrig) enthalten, und die [Reihenfolge in der Group by](-search-sql-orderingroup.md) -Klausel kann jede Gruppe mit unterschiedlichen Regeln sortieren.</span><span class="sxs-lookup"><span data-stu-id="4060c-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="4060c-131">Weitere Informationen finden Sie im nachfolgenden Abschnitt [Bestell Gruppen](#ordering-groups) .</span><span class="sxs-lookup"><span data-stu-id="4060c-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="4060c-132">Gruppen Bereiche</span><span class="sxs-lookup"><span data-stu-id="4060c-132">Group Ranges</span></span>

<span data-ttu-id="4060c-133">In der folgenden Tabelle wird veranschaulicht, wie die Ergebnisse in Gruppen unterteilt werden, basierend auf den Bereichs Limits:</span><span class="sxs-lookup"><span data-stu-id="4060c-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="4060c-134">Beispiel ( <column> \[ Gruppen Bereiche \] )</span><span class="sxs-lookup"><span data-stu-id="4060c-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="4060c-135">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="4060c-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4060c-136">System. size \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="4060c-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="4060c-137">Die Ergebnisse werden in vier Bucket gruppiert: **MinValue**: Size < 1000</span><span class="sxs-lookup"><span data-stu-id="4060c-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="4060c-138">**1000:** 1000 <= Größe < 5000</span><span class="sxs-lookup"><span data-stu-id="4060c-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="4060c-139">**5000:** Größe >= 5000</span><span class="sxs-lookup"><span data-stu-id="4060c-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="4060c-140">**Null:** Kein Wert für Größe</span><span class="sxs-lookup"><span data-stu-id="4060c-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="4060c-141">System. Author \[ vor ('m '), After (' r ')\]</span><span class="sxs-lookup"><span data-stu-id="4060c-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="4060c-142">Die Ergebnisse werden in vier Bucket gruppiert: **MinValue:** "Autor < Zeichen" vor "m"</span><span class="sxs-lookup"><span data-stu-id="4060c-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="4060c-143">**m:** Zeichen vor "m" <= Autor < Zeichen nach "r"</span><span class="sxs-lookup"><span data-stu-id="4060c-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="4060c-144">**r:** Zeichen nach "r" <= Autor</span><span class="sxs-lookup"><span data-stu-id="4060c-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="4060c-145">**Null:** Kein Wert für Autor</span><span class="sxs-lookup"><span data-stu-id="4060c-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="4060c-146">System. Author \[ MinValue/"a to l", "m"/be to z "\]</span><span class="sxs-lookup"><span data-stu-id="4060c-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="4060c-147">Die Ergebnisse werden in drei Bucket gruppiert: **a bis l:** Author < "m"</span><span class="sxs-lookup"><span data-stu-id="4060c-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="4060c-148">**m bis z:** "m" <= Autor</span><span class="sxs-lookup"><span data-stu-id="4060c-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="4060c-149">**Null:** Kein Wert für Autor</span><span class="sxs-lookup"><span data-stu-id="4060c-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="4060c-150">System. DateCreated \[ "2005-1-01", "2006-6-01"\]</span><span class="sxs-lookup"><span data-stu-id="4060c-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="4060c-151">Die Ergebnisse werden in vier Bucket gruppiert:</span><span class="sxs-lookup"><span data-stu-id="4060c-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="4060c-152">**MinValue:** DateCreated-< 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="4060c-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="4060c-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="4060c-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="4060c-154">**2006-1-01:** DateCreated->= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="4060c-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="4060c-155">**Null:** Kein Wert für DateCreated</span><span class="sxs-lookup"><span data-stu-id="4060c-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="4060c-156">Korre `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="4060c-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="4060c-157">Richtig: `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="4060c-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="4060c-158">Bezeichnen von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-158">Labeling Groups</span></span>

<span data-ttu-id="4060c-159">Um die Lesbarkeit zu verbessern, können Sie Gruppen mit der folgenden Syntax bezeichnen:</span><span class="sxs-lookup"><span data-stu-id="4060c-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="4060c-160">Die Bezeichnung ist von der Bereichs Beschränkung mit einem Schrägstrich getrennt und in einfache Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4060c-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="4060c-161">Wenn Sie keine Bezeichnung angeben, ist der Gruppenname die Zeichenfolge für das Bereichs Limit.</span><span class="sxs-lookup"><span data-stu-id="4060c-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="4060c-162">Im folgenden finden Sie ein Beispiel für die Bezeichnung von Gruppen:</span><span class="sxs-lookup"><span data-stu-id="4060c-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="4060c-163">In Windows 7 oder höher können Sie auch eine generische \[ andere Bezeichnung verwenden, \] um mehrere Gruppierungs Bereiche zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="4060c-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="4060c-164">Ergebnisse aus allen Gruppen, die mit dieser Bezeichnung identifiziert werden, werden mit dieser Bezeichnung zu einer Gruppe zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="4060c-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="4060c-165">Diese Ergebnis Gruppe wird nach allen anderen Gruppen außer der **null** -Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4060c-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="4060c-166">Die Gruppe **null** enthält Ergebnisse für Elemente, die nicht über einen Wert für die angegebene Eigenschaft verfügen.</span><span class="sxs-lookup"><span data-stu-id="4060c-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="4060c-167">Vor Windows 7 wird die \[ andere \] Bezeichnung wie jede andere Gruppen Bezeichnung behandelt.</span><span class="sxs-lookup"><span data-stu-id="4060c-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="4060c-168">Der folgende Code ist ein Beispiel für die Verwendung der \[ anderen \] Bezeichnung für Gruppen, die in Windows 7 oder höher erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="4060c-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="4060c-169">In der folgenden Tabelle sind die Gruppen aufgeführt, die durch den vorangehenden Gruppierungs Code in Windows 7 oder höher erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="4060c-170">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="4060c-170">Group</span></span>     | <span data-ttu-id="4060c-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="4060c-171">System.Author</span></span> | <span data-ttu-id="4060c-172">System. filename</span><span class="sxs-lookup"><span data-stu-id="4060c-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="4060c-173">0</span><span class="sxs-lookup"><span data-stu-id="4060c-173">0</span></span>         | <span data-ttu-id="4060c-174">1 Rechnung</span><span class="sxs-lookup"><span data-stu-id="4060c-174">1Bill</span></span>         | <span data-ttu-id="4060c-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-175">Lorem.docx</span></span>      |
| <span data-ttu-id="4060c-176">Q</span><span class="sxs-lookup"><span data-stu-id="4060c-176">Q</span></span>         | <span data-ttu-id="4060c-177">Queen</span><span class="sxs-lookup"><span data-stu-id="4060c-177">Queen</span></span>         | <span data-ttu-id="4060c-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="4060c-179">Robin</span><span class="sxs-lookup"><span data-stu-id="4060c-179">Robin</span></span>         | <span data-ttu-id="4060c-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-180">dolor.docx</span></span>      |
| <span data-ttu-id="4060c-181">J</span><span class="sxs-lookup"><span data-stu-id="4060c-181">Y</span></span>         | <span data-ttu-id="4060c-182">Kette</span><span class="sxs-lookup"><span data-stu-id="4060c-182">Zara</span></span>          | <span data-ttu-id="4060c-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-183">amet.docx</span></span>       |
| <span data-ttu-id="4060c-184">\[Außer\]</span><span class="sxs-lookup"><span data-stu-id="4060c-184">\[OTHER\]</span></span> | <span data-ttu-id="4060c-185">Abner</span><span class="sxs-lookup"><span data-stu-id="4060c-185">Abner</span></span>         | <span data-ttu-id="4060c-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="4060c-187">Bernd</span><span class="sxs-lookup"><span data-stu-id="4060c-187">Bob</span></span>           | <span data-ttu-id="4060c-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="4060c-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="4060c-189">Xaria</span></span>         | <span data-ttu-id="4060c-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-190">magna.docx</span></span>      |
| <span data-ttu-id="4060c-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="4060c-191">**NULL**</span></span>  |               | <span data-ttu-id="4060c-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="4060c-193">Anordnen von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-193">Ordering Groups</span></span>

<span data-ttu-id="4060c-194">Es gibt drei Möglichkeiten, um Elemente in Gruppen zu sortieren:</span><span class="sxs-lookup"><span data-stu-id="4060c-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="4060c-195">Standardsortierung: Wenn Sie nichts anderes angeben, werden die Ergebnisse nach den Werten in der Spalte Gruppieren in aufsteigender Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="4060c-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="4060c-196">Order by: Sie können eine absteigende Reihenfolge in einer ORDER BY-Klausel angeben.</span><span class="sxs-lookup"><span data-stu-id="4060c-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="4060c-197">Sie müssen die Ergebnisse nach der Spalte Gruppieren in sortieren.</span><span class="sxs-lookup"><span data-stu-id="4060c-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="4060c-198">Order in Group by: Sie können für jede Gruppe eine andere Reihenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="4060c-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="4060c-199">Wenn Sie [System. Kind](../properties/props-system-kind.md)gruppieren, können Sie Dokumente nach System [. Author](../properties/props-system-author.md) und Musik von [System. Music.](../properties/props-system-music-artist.md)Author anordnen.</span><span class="sxs-lookup"><span data-stu-id="4060c-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="4060c-200">Weitere Informationen zum Sortieren von Ergebnissen finden Sie in den Referenzseiten [Order By-Klausel](-search-sql-orderby.md) und [Order in Group-Klausel](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="4060c-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="4060c-201">Schachteln von Gruppen</span><span class="sxs-lookup"><span data-stu-id="4060c-201">Nesting Groups</span></span>

<span data-ttu-id="4060c-202">Gruppen können mit mehreren Group on-Klauseln geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="4060c-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="4060c-203">Die in der Abfrage angegebene Reihenfolge wird direkt in der Ausgabe Gruppen Hierarchie reflektiert, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="4060c-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="4060c-204">System. Kind</span><span class="sxs-lookup"><span data-stu-id="4060c-204">System.Kind</span></span>    | <span data-ttu-id="4060c-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="4060c-205">System.Author</span></span> | <span data-ttu-id="4060c-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="4060c-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="4060c-207">Dokumente</span><span class="sxs-lookup"><span data-stu-id="4060c-207">documents</span></span>      | <span data-ttu-id="4060c-208">Willa</span><span class="sxs-lookup"><span data-stu-id="4060c-208">Willa</span></span>         | <span data-ttu-id="4060c-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="4060c-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="4060c-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="4060c-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="4060c-211">Kette</span><span class="sxs-lookup"><span data-stu-id="4060c-211">Zara</span></span>          | <span data-ttu-id="4060c-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="4060c-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="4060c-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="4060c-213">2007-09-10</span></span>         |
| <span data-ttu-id="4060c-214">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="4060c-214">communications</span></span> | <span data-ttu-id="4060c-215">Abner</span><span class="sxs-lookup"><span data-stu-id="4060c-215">Abner</span></span>         | <span data-ttu-id="4060c-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="4060c-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="4060c-217">Jean</span><span class="sxs-lookup"><span data-stu-id="4060c-217">Jean</span></span>          | <span data-ttu-id="4060c-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="4060c-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="4060c-219">Willa</span><span class="sxs-lookup"><span data-stu-id="4060c-219">Willa</span></span>         | <span data-ttu-id="4060c-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="4060c-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="4060c-221">Kette</span><span class="sxs-lookup"><span data-stu-id="4060c-221">Zara</span></span>          | <span data-ttu-id="4060c-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="4060c-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="4060c-223">Gruppieren von Vektor Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4060c-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="4060c-224">Gruppieren von Vektor Eigenschaften, Eigenschaften, die einen oder mehrere Werte gleichzeitig enthalten können, vergleicht die Vektor Werte standardmäßig einzeln.</span><span class="sxs-lookup"><span data-stu-id="4060c-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="4060c-225">Wenn beispielsweise ein Dokument, Lorem.docx, mit der System. Author-Eigenschaft "Theresa;" vorhanden ist. Zara "und ein anderes Dokument, Ipsum.docx, mit der System. Author-Eigenschaft als" Zara ", gibt die Abfrage das Resultset in zwei Gruppen zurück, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="4060c-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="4060c-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="4060c-226">System.Author</span></span> | <span data-ttu-id="4060c-227">System. filename</span><span class="sxs-lookup"><span data-stu-id="4060c-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="4060c-228">SIAs</span><span class="sxs-lookup"><span data-stu-id="4060c-228">Theresa</span></span>       | <span data-ttu-id="4060c-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-229">Lorem.docx</span></span>      |
| <span data-ttu-id="4060c-230">Kette</span><span class="sxs-lookup"><span data-stu-id="4060c-230">Zara</span></span>          | <span data-ttu-id="4060c-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="4060c-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="4060c-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="4060c-233">Wie Sie sehen können, gibt die Gruppierung von Vektor Eigenschaften doppelte Zeilen zurück.</span><span class="sxs-lookup"><span data-stu-id="4060c-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="4060c-234">Lorem.docx wird zweimal angezeigt, weil es zwei Autoren hat.</span><span class="sxs-lookup"><span data-stu-id="4060c-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="4060c-235">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="4060c-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="4060c-236">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4060c-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4060c-237">Aggregatfunktionen</span><span class="sxs-lookup"><span data-stu-id="4060c-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="4060c-238">Order By-Klausel</span><span class="sxs-lookup"><span data-stu-id="4060c-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="4060c-239">Order in Group-Klausel</span><span class="sxs-lookup"><span data-stu-id="4060c-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
