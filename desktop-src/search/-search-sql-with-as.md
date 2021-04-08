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
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="5642b-104">WITH--as Group Alias-Prädikat</span><span class="sxs-lookup"><span data-stu-id="5642b-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="5642b-105">Spalten Gruppen Aliase bieten eine Möglichkeit, kürzere Namen anstelle des Namens einer Spalte oder einer Gruppe von Spalten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5642b-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="5642b-106">Das optionale Gruppenalias-Prädikat ist Teil der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="5642b-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="5642b-107">Die Syntax folgt:</span><span class="sxs-lookup"><span data-stu-id="5642b-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="5642b-108">Sie können mehr als einen Gruppenalias angeben, indem Sie den durch... Als Prädikate durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="5642b-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="5642b-109">Wenn in einem WHERE-Klausel-Prädikat auf einen gruppeneralias verwiesen wird, wird die Bedingung auf jede Spalte in der Gruppe angewendet.</span><span class="sxs-lookup"><span data-stu-id="5642b-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="5642b-110">Die logischen Werte, die sich aus der Übereinstimmung der einzelnen Spalten ergeben, werden mithilfe des logischen **or** -Operators kombiniert.</span><span class="sxs-lookup"><span data-stu-id="5642b-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="5642b-111">Ein Alias muss definiert werden, bevor er verwendet werden kann, und er kann nur innerhalb der WHERE-Klausel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5642b-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="5642b-112">Der Aliasname muss ein regulärer Bezeichner sein, dem ein erforderliches Nummern Zeichen () vorangestellt ist \# .</span><span class="sxs-lookup"><span data-stu-id="5642b-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="5642b-113">Der Spalten Bezeichner kann einen oder mehrere Spalten Spezifizierer enthalten, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="5642b-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="5642b-114">Die Liste der Spalten muss in Klammern eingeschlossen werden, und jeder kann eine Gewichtung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5642b-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="5642b-115">Jede Spalte weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="5642b-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="5642b-116">Weitere Informationen zum Angeben von Spalten Gewichtungen finden Sie unter frei [Text Prädikat](-search-sql-freetext.md) und [enthält Prädikat](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="5642b-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="5642b-117">Der Spalten Bezeichner kann regulär oder getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="5642b-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="5642b-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5642b-118">Examples</span></span>

<span data-ttu-id="5642b-119">Die folgenden WHERE-klauselbeispiele veranschaulichen, wann und wie Sie das Gruppenalias Prädikat verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5642b-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="5642b-120">Das erste Beispiel zeigt eine immer wiederkehrende WHERE-Klausel, die keine Gruppen Aliasing verwendet.</span><span class="sxs-lookup"><span data-stu-id="5642b-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="5642b-121">Das vorherige Beispiel kann mithilfe eines Gruppenalias vereinfacht werden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5642b-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="5642b-122">Im folgenden finden Sie ein Beispiel für eine positive Gewichtung, bei der die **Title** -Eigenschaft bei der Bestimmung des relativen Rangs stärker gewichtet wird.</span><span class="sxs-lookup"><span data-stu-id="5642b-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="5642b-123">Im folgenden finden Sie ein Beispiel für eine negative Gewichtung, bei der die **Title** -Eigenschaft mit Gewichtung von 0 nicht berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="5642b-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="5642b-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5642b-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5642b-125">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="5642b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5642b-126">Frei Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="5642b-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="5642b-127">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5642b-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5642b-128">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="5642b-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="5642b-129">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="5642b-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



