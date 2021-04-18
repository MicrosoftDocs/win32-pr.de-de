---
description: Das LIKE-Prädikat führt einen Muster vergleichsvergleich für die angegebene Spalte aus.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340162"
---
# <a name="like-predicate"></a><span data-ttu-id="6dae0-103">LIKE-Prädikat</span><span class="sxs-lookup"><span data-stu-id="6dae0-103">LIKE Predicate</span></span>

<span data-ttu-id="6dae0-104">Das LIKE-Prädikat führt einen Muster vergleichsvergleich für die angegebene Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="6dae0-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="6dae0-105">Es verwendet die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="6dae0-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="6dae0-106"><column>Kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein.</span><span class="sxs-lookup"><span data-stu-id="6dae0-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="6dae0-107">Die-Spalte ist auf die Eigenschaften im Eigenschaften Speicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6dae0-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="6dae0-108">Der <Platzhalter \_ Literal> ist ein Zeichenfolgenliteral</span><span class="sxs-lookup"><span data-stu-id="6dae0-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="6dae0-109">Er ist in Anführungszeichen eingeschlossen und kann optional Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6dae0-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="6dae0-110">Die Match-Zeichenfolge kann bei Bedarf mehrere Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6dae0-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="6dae0-111">In der folgenden Tabelle werden die Platzhalter Zeichen beschrieben, die vom LIKE-Prädikat erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="6dae0-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="6dae0-112">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="6dae0-112">Wildcard</span></span>                | <span data-ttu-id="6dae0-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6dae0-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="6dae0-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6dae0-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dae0-115">% (Prozent)</span><span class="sxs-lookup"><span data-stu-id="6dae0-115">% (percent)</span></span>             | <span data-ttu-id="6dae0-116">Entspricht 0 (null) oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6dae0-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="6dae0-117">"Comp% r" entspricht "Comp", gefolgt von NULL oder mehr Zeichen, die auf eine r enden.</span><span class="sxs-lookup"><span data-stu-id="6dae0-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="6dae0-118">\_ (Unterstrich)</span><span class="sxs-lookup"><span data-stu-id="6dae0-118">\_ (underscore)</span></span>         | <span data-ttu-id="6dae0-119">Entspricht einem beliebigen einzelnen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6dae0-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="6dae0-120">"Comp \_ ter" entspricht "Comp", gefolgt von genau einem beliebigen Zeichen, gefolgt von "ter".</span><span class="sxs-lookup"><span data-stu-id="6dae0-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="6dae0-121">\[\](eckige Klammern)</span><span class="sxs-lookup"><span data-stu-id="6dae0-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="6dae0-122">Entspricht einem beliebigen einzelnen Zeichen innerhalb des angegebenen Bereichs oder der angegebenen Menge.</span><span class="sxs-lookup"><span data-stu-id="6dae0-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="6dae0-123">Beispielsweise \[ gibt a-z \] einen Bereich an. \[ AEIOU \] gibt den Satz von Vokalen an.</span><span class="sxs-lookup"><span data-stu-id="6dae0-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="6dae0-124">"Comp \[ a-z \] re" entspricht "Comp", gefolgt von einem einzelnen Zeichen im Bereich von a bis z, gefolgt von "be".</span><span class="sxs-lookup"><span data-stu-id="6dae0-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="6dae0-125">"Comp \[ Ao \] " entspricht "Comp", gefolgt von einem einzelnen Zeichen, das entweder ein oder ein o sein muss.</span><span class="sxs-lookup"><span data-stu-id="6dae0-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="6dae0-126">\[^ \] Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="6dae0-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="6dae0-127">Entspricht einem beliebigen einzelnen Zeichen, das nicht innerhalb des angegebenen Bereichs oder Satzes liegt.</span><span class="sxs-lookup"><span data-stu-id="6dae0-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="6dae0-128">Beispielsweise \[ gibt ^ a-z \] einen Bereich an, der a bis z ausschließt. \[ ^ AEIOU \] gibt eine Menge an, die Vokale ausschließt.</span><span class="sxs-lookup"><span data-stu-id="6dae0-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="6dae0-129">"Comp \[ ^ u \] " entspricht "Comp", gefolgt von einem einzelnen Zeichen, das kein u ist.</span><span class="sxs-lookup"><span data-stu-id="6dae0-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="6dae0-130">Wenn Sie Prädikate mit mehreren Bereichen erstellen, müssen die Bereiche in der richtigen Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6dae0-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="6dae0-131">Um die Platzhalter Zeichen als Literalzeichen für den Abgleich und nicht als Platzhalter Zeichen abzugleichen, platzieren Sie das Zeichen in eckigen Klammern.</span><span class="sxs-lookup"><span data-stu-id="6dae0-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="6dae0-132">Verwenden Sie z. b. "", um das Prozentzeichen abzugleichen. \[ % \]</span><span class="sxs-lookup"><span data-stu-id="6dae0-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="6dae0-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dae0-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="6dae0-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dae0-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6dae0-135">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="6dae0-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6dae0-136">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="6dae0-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="6dae0-137">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="6dae0-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="6dae0-138">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="6dae0-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="6dae0-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6dae0-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6dae0-140">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="6dae0-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="6dae0-141">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="6dae0-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




