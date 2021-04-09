---
description: Der ISABOUT-Begriff vergleicht Spalten mit einer Gruppe von mindestens einem Suchbegriff.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: ISABOUT-Begriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750384"
---
# <a name="isabout-term"></a><span data-ttu-id="6f3a2-103">ISABOUT-Begriff</span><span class="sxs-lookup"><span data-stu-id="6f3a2-103">ISABOUT Term</span></span>

<span data-ttu-id="6f3a2-104">**Veraltet**</span><span class="sxs-lookup"><span data-stu-id="6f3a2-104">**Deprecated**</span></span>

<span data-ttu-id="6f3a2-105">Diese Funktion wurde ab Windows 8 entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="6f3a2-106">Wenn Sie neue Anwendungen schreiben, sollten Sie diese veraltete Funktion nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="6f3a2-107">Wenn Sie vorhandene Anwendungen ändern, wird dringend empfohlen, jegliche Abhängigkeit von dieser Funktion zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="6f3a2-108">Der ISABOUT-Begriff vergleicht Spalten mit einer Gruppe von mindestens einem Suchbegriff.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="6f3a2-109">Es weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="6f3a2-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="6f3a2-110">Der optionale RankMethod-Begriff gibt die Berechnungsmethode an, mit der die mit einer oder mehreren Komponenten abgeglichen Dokumente eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="6f3a2-111">Wenn keine RankMethod angegeben ist, wird die standardmäßige Jaccard-Koeffizienten-Rang Folge Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="6f3a2-112">Der ISABOUT-Begriff kann über eine oder mehrere Komponenten verfügen.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="6f3a2-113">Die im-Prädikat [enthalten](-search-sql-contains.md) angegebenen Spalten werden für jede Komponente getestet.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="6f3a2-114">Das Dokument ist in den Ergebnissen enthalten, wenn mindestens eine der Komponenten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="6f3a2-115">Kommas trennen mehrere Komponenten.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-115">Commas separate multiple components.</span></span>

<span data-ttu-id="6f3a2-116">Der Komponenten Teil weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="6f3a2-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="6f3a2-117">Sie können den optionalen Gewichtungs Begriff verwenden, um die relative Wichtigkeit der einzelnen Begriffe innerhalb des ISABOUT-Begriffs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="6f3a2-118">Wenn kein Gewichtungs Begriff angewendet wird, wird die Standard Gewichtung 1,0 impliziert.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="6f3a2-119">In der folgenden Tabelle werden mögliche Übereinstimmungs Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f3a2-120">type</span><span class="sxs-lookup"><span data-stu-id="6f3a2-120">Type</span></span></th>
<th><span data-ttu-id="6f3a2-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f3a2-121">Description</span></span></th>
<th><span data-ttu-id="6f3a2-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f3a2-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f3a2-123">Word</span><span class="sxs-lookup"><span data-stu-id="6f3a2-123">Word</span></span></td>
<td><span data-ttu-id="6f3a2-124">Ein einzelnes Wort ohne Leerzeichen oder ein anderes Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-124">A single word without spaces or other punctuation.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f3a2-125">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="6f3a2-125">Phrase</span></span></td>
<td><span data-ttu-id="6f3a2-126">Mehrere Wörter oder enthaltene Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-126">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f3a2-127">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="6f3a2-127">Wildcard</span></span></td>
<td><span data-ttu-id="6f3a2-128">Wörter oder Ausdrücke mit dem Sternchen (\*) am Ende hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="6f3a2-129">Weitere Informationen finden Sie unter Verwenden von Platzhaltern <a href="-search-sql-wildcards.md">im enthält-Prädikat</a>.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="6f3a2-130">ISABOUT-Spalten Gewichtung</span><span class="sxs-lookup"><span data-stu-id="6f3a2-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="6f3a2-131">Der ISABOUT-Begriff ordnet den übereinstimmenden Dokumenten zu, je nachdem, wie genau jedes Dokument mit den übereinstimmenden Begriffen in der Abfrage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="6f3a2-132">Mit der Spalten Gewichtung können Sie eine größere Wichtigkeit beim Vergleichen einiger Vergleichs Begriffe als andere verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="6f3a2-133">Für jeden Vergleichs Begriff im ISABOUT-Begriff kann ein Gewichtungswert angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="6f3a2-134">Die Gewichtung wird auf einen einzelnen Übereinstimmungs Begriff angewendet und wird durch das Schlüsselwort "Weight" angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="6f3a2-135">Der Gewichtungs Begriff verfügt über zwei alternative Syntaxen:</span><span class="sxs-lookup"><span data-stu-id="6f3a2-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="6f3a2-136">Der Gewichtungswert muss zwischen 0 und 1,0 liegen und darf nicht mehr als drei Dezimalstellen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="6f3a2-137">Wenn ein Gewichtungswert außerhalb dieses Bereichs angegeben wird, führt dies zu einer Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="6f3a2-138">Der nicht gewichtete Rang Folge Wert für einen Begriff wird mit dem Gewichtungswert für den Begriff multipliziert.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="6f3a2-139">Wenn für einen Übereinstimmungs Begriff keine Gewichtung angegeben wird, wird der Standardwert 1,0 impliziert.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="6f3a2-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6f3a2-140">Example</span></span>

<span data-ttu-id="6f3a2-141">Im folgenden Beispiel werden Gewichtungen auf die zwei ISABOUT-Übereinstimmungs Bedingungen angewendet, wobei die Long-und Short-Syntax für Gewichtungswerte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f3a2-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="6f3a2-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f3a2-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6f3a2-143">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="6f3a2-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f3a2-144">Frei Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="6f3a2-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="6f3a2-145">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="6f3a2-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



