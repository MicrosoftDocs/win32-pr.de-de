---
description: Das NULL-Prädikat gibt an, ob das Dokument über einen Wert für die Spalte verfügt.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: NULL-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341187"
---
# <a name="null-predicate"></a><span data-ttu-id="03cb7-103">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="03cb7-103">NULL Predicate</span></span>

<span data-ttu-id="03cb7-104">Das **null** -Prädikat gibt an, ob das Dokument über einen Wert für die Spalte verfügt.</span><span class="sxs-lookup"><span data-stu-id="03cb7-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="03cb7-105">Das **null** -Prädikat weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="03cb7-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="03cb7-106">Das optionale not-Schlüsselwort negiert das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="03cb7-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="03cb7-107">Die Spalte kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein.</span><span class="sxs-lookup"><span data-stu-id="03cb7-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03cb7-108">Um zu testen, ob eine Spalte den **null** -Wert aufweist, müssen Sie das **null** -Prädikat verwenden.</span><span class="sxs-lookup"><span data-stu-id="03cb7-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="03cb7-109">Die Verwendung des **null** -Werts in einem Vergleichs Prädikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="03cb7-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="03cb7-110">"Where column is **null**" ist richtig.</span><span class="sxs-lookup"><span data-stu-id="03cb7-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="03cb7-111">"Where Column = **null**" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="03cb7-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="03cb7-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="03cb7-112">Example</span></span>

<span data-ttu-id="03cb7-113">Im folgenden Beispiel werden Dokumente zurückgegeben, die keinen System. Video. Director-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="03cb7-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="03cb7-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03cb7-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="03cb7-115">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="03cb7-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="03cb7-116">LIKE-Prädikat</span><span class="sxs-lookup"><span data-stu-id="03cb7-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="03cb7-117">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="03cb7-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="03cb7-118">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="03cb7-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="03cb7-119">**Licher**</span><span class="sxs-lookup"><span data-stu-id="03cb7-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03cb7-120">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="03cb7-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="03cb7-121">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="03cb7-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



