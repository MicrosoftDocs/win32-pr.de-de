---
description: Der Near-Begriff wird verwendet, um anzugeben, dass zwei Inhalts Suchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das enthält-Prädikat erkannt zu werden.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: Near-Term
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342958"
---
# <a name="near-term"></a><span data-ttu-id="b55a7-103">Near-Term</span><span class="sxs-lookup"><span data-stu-id="b55a7-103">NEAR Term</span></span>

<span data-ttu-id="b55a7-104">Der Near-Begriff wird verwendet, um anzugeben, dass zwei Inhalts Suchbegriffe relativ nah beieinander liegen müssen, um als Übereinstimmung für das [enthält](-search-sql-contains.md) -Prädikat erkannt zu werden.</span><span class="sxs-lookup"><span data-stu-id="b55a7-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="b55a7-105">Die Syntax für den NEAR-Begriff lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b55a7-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="b55a7-106">Der Near-Begriff kann durch das Schlüsselwort "Near" oder durch eine Tilde (~) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b55a7-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="b55a7-107">Wenn die mit Near in der Abfrage verbundenen Wörter innerhalb der Spalte, die durchsucht wird, innerhalb von ungefähr 50 Wörtern zueinander gefunden werden, gibt der Near-Begriff eine Übereinstimmung zurück.</span><span class="sxs-lookup"><span data-stu-id="b55a7-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="b55a7-108">Je näher die beiden Wörter sind, desto höher ist der berechnete Rang für den NEAR-Begriff.</span><span class="sxs-lookup"><span data-stu-id="b55a7-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="b55a7-109">Je weiter auseinander die beiden Wörter liegen, desto niedriger ist der Rang.</span><span class="sxs-lookup"><span data-stu-id="b55a7-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="b55a7-110">Die Anzahl von Wörtern zwischen gefundenen Suchbegriffen ist ungefähre Werte und hängt von der Darstellung von Füll Wörtern ab, wie z. b. "a" oder "The" und der Art und Weise, wie Wörter Trennungen Text mit Token versehen.</span><span class="sxs-lookup"><span data-stu-id="b55a7-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="b55a7-111">Der Wert ist möglicherweise kleiner als 50.</span><span class="sxs-lookup"><span data-stu-id="b55a7-111">It may be less than 50.</span></span>

 


<span data-ttu-id="b55a7-112">In der folgenden Tabelle werden die Typen der Inhalts Suchbegriffe beschrieben, die mit einem NEAR-Begriff in einem enthält-Prädikat verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b55a7-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b55a7-113">type</span><span class="sxs-lookup"><span data-stu-id="b55a7-113">Type</span></span></th>
<th><span data-ttu-id="b55a7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b55a7-114">Description</span></span></th>
<th><span data-ttu-id="b55a7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b55a7-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b55a7-116">Word</span><span class="sxs-lookup"><span data-stu-id="b55a7-116">Word</span></span></td>
<td><span data-ttu-id="b55a7-117">Ein einzelnes Wort ohne Leerzeichen oder ein anderes Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b55a7-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="b55a7-118">Doppelte Anführungszeichen sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b55a7-118">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b55a7-119">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="b55a7-119">Phrase</span></span></td>
<td><span data-ttu-id="b55a7-120">Mehrere Wörter oder enthaltene Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="b55a7-120">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b55a7-121">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="b55a7-121">Wildcard</span></span></td>
<td><span data-ttu-id="b55a7-122">Wörter oder Ausdrücke mit dem Sternchen (\*) am Ende hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b55a7-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="b55a7-123">Weitere Informationen finden Sie unter Verwenden von Platzhaltern <a href="-search-sql-wildcards.md">im enthält-Prädikat</a>.</span><span class="sxs-lookup"><span data-stu-id="b55a7-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="b55a7-124">Wenn die mit dem NEAR-Begriff angegebenen Übereinstimmungs Wörter in der Spalte gefunden werden, die durchsucht wird, die aber weiter auseinander liegen als 50 Wörter, wird das Ergebnis trotzdem zurückgegeben, aber hat den [Rang](-search-sql-understandingrelevancevalues.md) 0.</span><span class="sxs-lookup"><span data-stu-id="b55a7-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="b55a7-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b55a7-125">Example</span></span>

<span data-ttu-id="b55a7-126">Im folgenden Beispiel wird die Verkettung von Near-Begriffen mithilfe der kurzen und langen Formen der Laufzeit veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b55a7-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="b55a7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b55a7-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b55a7-128">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="b55a7-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b55a7-129">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="b55a7-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="b55a7-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b55a7-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b55a7-131">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="b55a7-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="b55a7-132">Verwenden von Platzhaltern im enthält-Prädikat</span><span class="sxs-lookup"><span data-stu-id="b55a7-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



