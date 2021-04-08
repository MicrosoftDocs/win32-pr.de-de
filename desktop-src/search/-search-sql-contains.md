---
description: Das enthält-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Enthält Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862155"
---
# <a name="contains-predicate"></a><span data-ttu-id="2fab8-103">Enthält Prädikat</span><span class="sxs-lookup"><span data-stu-id="2fab8-103">CONTAINS Predicate</span></span>

<span data-ttu-id="2fab8-104">Das enthält-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.</span><span class="sxs-lookup"><span data-stu-id="2fab8-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="2fab8-105">Das enthält ein Prädikat, das über Features für übereinstimmende Wörter, die Übereinstimmung von Flexions Formen von Wörtern, das Suchen mithilfe von Platzhalter Zeichen und die Suche mithilfe von Near verfügt</span><span class="sxs-lookup"><span data-stu-id="2fab8-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="2fab8-106">Sie können auch Gewichtungen in einem enthält-Prädikat anwenden, um die Wichtigkeit der Spalten festzulegen, in denen der Suchbegriff gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2fab8-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="2fab8-107">Das enthält-Prädikat eignet sich besser für exakte Übereinstimmungen (im Gegensatz zum frei [Text](-search-sql-freetext.md) Prädikat), das sich besser für die Suche nach Dokumenten eignet, die Kombinationen der in der Spalte verteilten Suchwörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fab8-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="2fab8-108">Bei Suchvorgängen wird nicht zwischen Groß- und Kleinschreibung unterschieden.</span><span class="sxs-lookup"><span data-stu-id="2fab8-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="2fab8-109">Im folgenden finden Sie die grundlegende Syntax des enthält-Prädikats:</span><span class="sxs-lookup"><span data-stu-id="2fab8-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="2fab8-110">Der voll Text \_ Spalten Verweis ist optional.</span><span class="sxs-lookup"><span data-stu-id="2fab8-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="2fab8-111">Damit können Sie die Suche auf eine einzelne Spalte oder eine Spalten Gruppe beschränken, für die das Prädikat "enthält" getestet wird.</span><span class="sxs-lookup"><span data-stu-id="2fab8-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="2fab8-112">Wenn die voll Text Spalte als "All" oder "" angegeben wird \* , werden alle indizierten Texteigenschaften durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2fab8-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="2fab8-113">Obwohl es sich bei der Spalte nicht um eine Text Eigenschaft handeln muss, können die Ergebnisse bedeutungslos sein, wenn es sich bei der Spalte um einen anderen Datentyp handelt.</span><span class="sxs-lookup"><span data-stu-id="2fab8-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="2fab8-114">Der Spaltenname kann entweder ein regulärer oder ein Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen.</span><span class="sxs-lookup"><span data-stu-id="2fab8-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="2fab8-115">Wenn keine voll Text Spalte angegeben ist, wird die Spalte "System. search. Content" verwendet, die den Hauptteil des Dokuments enthält.</span><span class="sxs-lookup"><span data-stu-id="2fab8-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="2fab8-116">Der LCID-Teil des Prädikats gibt das Suchgebiets Schema an.</span><span class="sxs-lookup"><span data-stu-id="2fab8-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="2fab8-117">Dies weist das Such Modul an, die entsprechende Wörter Trennung und die Flexions Formen für die Suchabfrage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2fab8-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="2fab8-118">Um das Gebiets Schema anzugeben, geben Sie den Windows-Standard Sprachcode Bezeichner (LCID) an.</span><span class="sxs-lookup"><span data-stu-id="2fab8-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="2fab8-119">Beispielsweise ist 1033 die LCID für USA-Englisch.</span><span class="sxs-lookup"><span data-stu-id="2fab8-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="2fab8-120">Platzieren Sie die LCID als letztes Element innerhalb der Klammern der enthaltene Klausel.</span><span class="sxs-lookup"><span data-stu-id="2fab8-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="2fab8-121">Wichtige Informationen zum Suchen von und Sprachen finden [Sie unter Verwenden lokalisierter Such](-search-sql-usinglocsearches.md)Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2fab8-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="2fab8-122">Das Standard Gebiets Schema für die Suche ist das Standard Gebiets Schema des Systems.</span><span class="sxs-lookup"><span data-stu-id="2fab8-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="2fab8-123">Der enthält Bedingungs \_ Teil muss in einfache Anführungszeichen eingeschlossen werden, um einzelne Wörter oder doppelte Anführungszeichen für Ausdrücke zu verwenden, und besteht aus einem oder mehreren Inhalts Suchbegriffen, die mithilfe der logischen Operatoren **and** oder **or** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="2fab8-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="2fab8-124">Sie können den optionalen unären Operator **nicht** hinter einem **and-** Operator verwenden, um den logischen Wert eines Inhalts Suchbegriffs zu negieren.</span><span class="sxs-lookup"><span data-stu-id="2fab8-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="2fab8-125">Der **Not** -Operator kann nur nach **und** auftreten.</span><span class="sxs-lookup"><span data-stu-id="2fab8-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="2fab8-126">Der **Not** -Operator kann nicht verwendet werden, wenn es nur eine Übereinstimmungs Bedingung gibt oder nach dem **or** -Operator.</span><span class="sxs-lookup"><span data-stu-id="2fab8-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="2fab8-127">Mit Klammern können Sie Inhalts Suchbegriffe gruppieren und Schachteln.</span><span class="sxs-lookup"><span data-stu-id="2fab8-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="2fab8-128">In der folgenden Tabelle wird die Rangfolge der logischen Operatoren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2fab8-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="2fab8-129">Reihenfolge (Rangfolge)</span><span class="sxs-lookup"><span data-stu-id="2fab8-129">Order (precedence)</span></span> | <span data-ttu-id="2fab8-130">Logischer Operator</span><span class="sxs-lookup"><span data-stu-id="2fab8-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="2fab8-131">First (höchste)</span><span class="sxs-lookup"><span data-stu-id="2fab8-131">First (highest)</span></span>    | <span data-ttu-id="2fab8-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="2fab8-132">**NOT**</span></span>          |
| <span data-ttu-id="2fab8-133">Sekunde</span><span class="sxs-lookup"><span data-stu-id="2fab8-133">Second</span></span>             | <span data-ttu-id="2fab8-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="2fab8-134">**AND**</span></span>          |
| <span data-ttu-id="2fab8-135">Dritte (niedrigste)</span><span class="sxs-lookup"><span data-stu-id="2fab8-135">Third (lowest)</span></span>     | <span data-ttu-id="2fab8-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="2fab8-136">**OR**</span></span>           |

<span data-ttu-id="2fab8-137">Logische Operatoren desselben Typs sind assoziativ, und es ist keine Berechnungs Reihenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="2fab8-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="2fab8-138">Beispielsweise können (a **und** B) **und** (c **und** d) (b **und** c) **und** (A **und** d) ohne Änderung im logischen Ergebnis berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="2fab8-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="2fab8-139">In der folgenden Tabelle werden die Typen der Inhalts Suchbegriffe beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2fab8-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2fab8-140">type</span><span class="sxs-lookup"><span data-stu-id="2fab8-140">Type</span></span></th>
<th><span data-ttu-id="2fab8-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fab8-141">Description</span></span></th>
<th><span data-ttu-id="2fab8-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fab8-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2fab8-143">Word</span><span class="sxs-lookup"><span data-stu-id="2fab8-143">Word</span></span></td>
<td><span data-ttu-id="2fab8-144">Ein einzelnes Wort ohne Leerzeichen oder ein anderes Interpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2fab8-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="2fab8-145">Doppelte Anführungszeichen sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2fab8-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fab8-146">Ausdruck</span><span class="sxs-lookup"><span data-stu-id="2fab8-146">Phrase</span></span></td>
<td><span data-ttu-id="2fab8-147">Mehrere Wörter oder enthaltene Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="2fab8-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fab8-148">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="2fab8-148">Wildcard</span></span></td>
<td><span data-ttu-id="2fab8-149">Wörter oder Ausdrücke mit dem Sternchen (\*) am Ende hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2fab8-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="2fab8-150">Weitere Informationen finden Sie unter Verwenden von Platzhaltern <a href="-search-sql-wildcards.md">im enthält-Prädikat</a>.</span><span class="sxs-lookup"><span data-stu-id="2fab8-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fab8-151">Voll Text Spalte</span><span class="sxs-lookup"><span data-stu-id="2fab8-151">Full-text Column</span></span></td>
<td><span data-ttu-id="2fab8-152">Der Name einer Eigenschaften Spalte, mit der die verbleibende Abfrage abgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fab8-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fab8-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="2fab8-153">Boolean</span></span></td>
<td><span data-ttu-id="2fab8-154">Wörter, Ausdrücke und Platzhalter Zeichenfolgen in Kombination mit den booleschen Operatoren <strong>and</strong>, <strong>or</strong>oder <strong>Not</strong>.</span><span class="sxs-lookup"><span data-stu-id="2fab8-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="2fab8-155">Schließen Sie die booleschen Begriffe in doppelte Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="2fab8-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fab8-156">Near</span><span class="sxs-lookup"><span data-stu-id="2fab8-156">Near</span></span></td>
<td><span data-ttu-id="2fab8-157">Wörter, Ausdrücke oder Platzhalter, getrennt durch die-Funktion in der Nähe von.</span><span class="sxs-lookup"><span data-stu-id="2fab8-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="2fab8-158">Weitere Informationen finden Sie unter <a href="-search-sql-near.md">near Term</a>.</span><span class="sxs-lookup"><span data-stu-id="2fab8-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2fab8-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="2fab8-159">FormsOf</span></span></td>
<td><span data-ttu-id="2fab8-160">Entspricht einem Wort und den Flexions Versionen dieses Worts.</span><span class="sxs-lookup"><span data-stu-id="2fab8-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="2fab8-161">Weitere Informationen finden Sie unter <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span><span class="sxs-lookup"><span data-stu-id="2fab8-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2fab8-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="2fab8-162">IsAbout</span></span></td>
<td><span data-ttu-id="2fab8-163">Kombiniert übereinstimmende Ergebnisse über mehrere Wort-, Ausdrucks-oder Platzhalter Suchbegriffe.</span><span class="sxs-lookup"><span data-stu-id="2fab8-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="2fab8-164">Jeder Suchbegriff kann optional gewichtet werden.</span><span class="sxs-lookup"><span data-stu-id="2fab8-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="2fab8-165">Optional können Sie die Rang Berechnungsmethode angeben, mit der Gewichtungen und die Anzahl der Elemente kombiniert werden, mit denen das Dokument übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2fab8-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="2fab8-166">Weitere Informationen finden Sie unter <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span><span class="sxs-lookup"><span data-stu-id="2fab8-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

<span data-ttu-id="2fab8-167">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="2fab8-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="2fab8-168">Verwenden von Platzhaltern im enthält-Prädikat</span><span class="sxs-lookup"><span data-stu-id="2fab8-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="2fab8-169">FORMSOF-Begriff</span><span class="sxs-lookup"><span data-stu-id="2fab8-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="2fab8-170">ISABOUT-Begriff</span><span class="sxs-lookup"><span data-stu-id="2fab8-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="2fab8-171">Near-Term</span><span class="sxs-lookup"><span data-stu-id="2fab8-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="2fab8-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fab8-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="2fab8-173">Referenz</span><span class="sxs-lookup"><span data-stu-id="2fab8-173">Reference</span></span>

[<span data-ttu-id="2fab8-174">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="2fab8-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="2fab8-175">Konzept</span><span class="sxs-lookup"><span data-stu-id="2fab8-175">Conceptual</span></span>

[<span data-ttu-id="2fab8-176">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="2fab8-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="2fab8-177">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="2fab8-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
