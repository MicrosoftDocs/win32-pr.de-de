---
description: Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden durch die WHERE-Klausel angegeben.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: WHERE-Klausel (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344674"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="c02ef-103">WHERE-Klausel (Windows-Suche)</span><span class="sxs-lookup"><span data-stu-id="c02ef-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="c02ef-104">Die Bedingungen, die bestimmen, ob ein Dokument in den von der Abfrage zurückgegebenen Ergebnissen enthalten ist, werden durch die WHERE-Klausel angegeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="c02ef-105">Auf der höchsten Ebene gibt es zwei Teile der Syntax der WHERE-Klausel:</span><span class="sxs-lookup"><span data-stu-id="c02ef-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="c02ef-106">Der optionale <\_ Gruppenalias> Teil der-Klausel vereinfacht komplexe Abfragen, indem einer Gruppe von mindestens einer Spalte ein Alias zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c02ef-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="c02ef-107">Dies kann die Lesbarkeit komplexer Abfragen verbessern, die über mehrere durch URLs angegebene Spalten hinweg nach denselben Informationen suchen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="c02ef-108">Weitere Informationen zu Gruppen Aliasen finden Sie unter [with-as Group Alias Predicate](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="c02ef-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="c02ef-109">Der <search condition> Teil der WHERE-Klausel ist ein oder mehrere Such Prädikate, die übereinstimmende Kriterien für die Suche angeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="c02ef-110">Such Prädikate sind Ausdrücke, die einige Fakten über einen Wert bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="c02ef-111">Das Ergebnis einer Such Bedingung ist ein boolescher Wert, entweder **true** , wenn das Dokument die angegebenen Suchbedingungen erfüllt, oder **false** , wenn dies nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c02ef-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="c02ef-112">Wenn das Ergebnis **true** ist, wird das Dokument zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="c02ef-113">Wenn das Ergebnis **false** ist, wird das Dokument nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="c02ef-114">Bei Dokumenten, die in einer Microsoft Windows Search-Abfrage zurückgegeben werden, werden Rang Werte entsprechend der Übereinstimmung der Suchbedingungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="c02ef-115">Jede der Abfrage Suchbedingungen kann eine [rankby](-search-sql-rankby.md) -Klausel enthalten, die das Ändern der zurückgegebenen Rang Werte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c02ef-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="c02ef-116">Die [reusewhere-Funktion](-search-sql-reusewhere.md) macht mehrere Abfragen, die die gleichen Suchbedingungen verwenden, effizienter.</span><span class="sxs-lookup"><span data-stu-id="c02ef-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="c02ef-117">Die WHERE-Klausel in einer Abfrage gibt den Satz von Elementen an, die in einer Abfrage gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c02ef-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="c02ef-118">Nachfolgende Abfragen können die Arbeit, die für die vorherige Auswertung ausgeführt wird, mithilfe der Funktion reusewhere in der neuen Abfrage WHERE-Klausel freigeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="c02ef-119">Such Prädikate</span><span class="sxs-lookup"><span data-stu-id="c02ef-119">Search Predicates</span></span>

<span data-ttu-id="c02ef-120">Eine Such Bedingung besteht aus einem oder mehreren Prädikaten oder Suchbedingungen, die beschreiben, wie der Benutzer sucht (z. b. wenn System. DateCreated > "2006-04-19").</span><span class="sxs-lookup"><span data-stu-id="c02ef-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="c02ef-121">Such Prädikate können mit den logischen Operatoren **and**, **or** oder **Not** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c02ef-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="c02ef-122">Der optionale unäre Operator **Not** kann nur mit **und** und nur verwendet werden, um den logischen Wert eines Prädikats oder einer Such Bedingung zu negieren.</span><span class="sxs-lookup"><span data-stu-id="c02ef-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="c02ef-123">Sie können Klammern verwenden, um logische Begriffe zu gruppieren und zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="c02ef-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="c02ef-124">Die folgende Tabelle zeigt die Rangfolge der logischen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="c02ef-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="c02ef-125">Reihenfolge (Rangfolge)</span><span class="sxs-lookup"><span data-stu-id="c02ef-125">Order (precedence)</span></span> | <span data-ttu-id="c02ef-126">Logischer Operator</span><span class="sxs-lookup"><span data-stu-id="c02ef-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="c02ef-127">First (höchste)</span><span class="sxs-lookup"><span data-stu-id="c02ef-127">First (highest)</span></span>    | <span data-ttu-id="c02ef-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="c02ef-128">**NOT**</span></span>          |
| <span data-ttu-id="c02ef-129">Sekunde</span><span class="sxs-lookup"><span data-stu-id="c02ef-129">Second</span></span>             | <span data-ttu-id="c02ef-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="c02ef-130">**AND**</span></span>          |
| <span data-ttu-id="c02ef-131">Dritte (niedrigste)</span><span class="sxs-lookup"><span data-stu-id="c02ef-131">Third (lowest)</span></span>     | <span data-ttu-id="c02ef-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="c02ef-132">**OR**</span></span>           |



 

<span data-ttu-id="c02ef-133">Logische Operatoren desselben Typs sind assoziativ, und es ist keine Berechnungs Reihenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="c02ef-134">Beispielsweise können (a **und** B) **und** (c **und** d) (a **und** d) **und** (B **und** C) ohne Änderung im logischen Ergebnis berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c02ef-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c02ef-135">Falsch: Where **Not** enthält (' Computer ')</span><span class="sxs-lookup"><span data-stu-id="c02ef-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="c02ef-136">Richtig: Where enthält ("Software") **und enthält keine** ("Computer").</span><span class="sxs-lookup"><span data-stu-id="c02ef-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="c02ef-137">In komplexen Abfragen möchten Sie möglicherweise mehr Akzente in einigen Spalten als in anderen Spalten platzieren.</span><span class="sxs-lookup"><span data-stu-id="c02ef-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="c02ef-138">Wenn Sie z. b. nach Dokumenten suchen, in denen "Software Design" erläutert wird, ist die Suche nach dem Suchbegriff im Dokumenttitel wahrscheinlich eine gute Frage, als die einzelnen Wörter im Text des Dokuments zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="c02ef-139">Um die Rangfolge von Dokumenten auf diese Weise zu beeinflussen, unterstützt die Microsoft Windows Search-Abfragesprache das Abwägen der Suchbedingungen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="c02ef-140">Weitere Informationen zur Spalten Gewichtung finden Sie unter [enthält ein Prädikat](-search-sql-contains.md) und ein frei [Text Prädikat](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="c02ef-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="c02ef-141">Es gibt drei Gruppen von Such Prädikaten in Windows Search: Volltext, nicht Volltext und Ordner Tiefe suchen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="c02ef-142">Prädikate für die Volltextsuche entsprechen in der Regel der Bedeutung von Inhalt, Titel und anderen Spalten und unterstützen die linguistische Übereinstimmung (z. b. Alternative Word-Formulare, Ausdrücke und Near-Suche).</span><span class="sxs-lookup"><span data-stu-id="c02ef-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="c02ef-143">Im Gegensatz dazu entsprechen nicht-voll Text Suchprädikate dem Wert der angegebenen Spalten und enthalten keine besondere linguistische Verarbeitung, aber in einigen Fällen bieten Zeichen basierten Musterabgleich.</span><span class="sxs-lookup"><span data-stu-id="c02ef-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="c02ef-144">Mit den Prädikaten für die Ordner Tiefe wird der Suchbereich auf einen angegebenen Pfad beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c02ef-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="c02ef-145">Wenn die Abfrage ein Dokument zurückgibt, weil ein nicht-voll Text Prädikat für dieses Dokument **true** ergibt, wird der Rangwert als 1000 berechnet.</span><span class="sxs-lookup"><span data-stu-id="c02ef-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="c02ef-146">Durch die Verwendung der Rang Umwandlungs [Funktion](-search-sql-rankby.md) kann der Rangwert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c02ef-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="c02ef-147">In den folgenden Tabellen werden die Prädikate für Volltext-, nicht-Volltext-und Ordner Tiefe-Suche beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c02ef-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="c02ef-148">Volltext-Prädikat</span><span class="sxs-lookup"><span data-stu-id="c02ef-148">Full-text predicate</span></span>                  | <span data-ttu-id="c02ef-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c02ef-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c02ef-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="c02ef-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="c02ef-151">Unterstützt komplexe Suchvorgänge für Begriffe in Dokument Textspalten (z. b. Titel, Inhalt).</span><span class="sxs-lookup"><span data-stu-id="c02ef-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="c02ef-152">Kann nach inflektierte Formen der Suchbegriffe suchen, auf die Nähe der Begriffe testen und logische Vergleiche durchführen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="c02ef-153">Suchbegriffe können Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c02ef-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="c02ef-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="c02ef-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="c02ef-155">Sucht nach Dokumenten, die der Bedeutung des Such Ausdrucks entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="c02ef-156">Verwandte Wörter und ähnliche Ausdrücke stimmen überein, wobei die Rang Spalte auf der Grundlage der Übereinstimmung des Dokuments mit dem Suchbegriff berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c02ef-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="c02ef-157">Suchbegriffe dürfen keine Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c02ef-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="c02ef-158">Nicht-voll Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="c02ef-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="c02ef-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c02ef-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c02ef-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="c02ef-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="c02ef-161">Spaltenwerte werden mithilfe eines einfachen Musterabgleich mit Platzhaltern verglichen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="c02ef-162">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="c02ef-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="c02ef-163">Spaltenwerte werden mit Zeichen folgen-, Datums-, Zeitstempel-, numerischen und anderen Literalwerten verglichen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="c02ef-164">Dieses Prädikat unterstützt Gleichheit und Ungleichheiten wie "größer als" und "kleiner als".</span><span class="sxs-lookup"><span data-stu-id="c02ef-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="c02ef-165">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="c02ef-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="c02ef-166">Mehrwertige Spalten werden mit einem mehrwertigen Array von literalen verglichen.</span><span class="sxs-lookup"><span data-stu-id="c02ef-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="c02ef-167">NULL</span><span class="sxs-lookup"><span data-stu-id="c02ef-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="c02ef-168">Spaltenwerte, die für das Dokument nicht definiert sind, können mithilfe des **null** -Prädikats erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="c02ef-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="c02ef-169">Ordner Tiefe</span><span class="sxs-lookup"><span data-stu-id="c02ef-169">Folder Depth</span></span>                             | <span data-ttu-id="c02ef-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c02ef-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c02ef-171">Umfang</span><span class="sxs-lookup"><span data-stu-id="c02ef-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="c02ef-172">Führt einen tiefen Durchlauf des angegebenen Pfads aus, einschließlich des jeweiligen Ordners und aller Unterordner.</span><span class="sxs-lookup"><span data-stu-id="c02ef-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="c02ef-173">Befinden</span><span class="sxs-lookup"><span data-stu-id="c02ef-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="c02ef-174">Führt einen flachen Durchlauf des angegebenen Pfads durch und sucht nur nach dem jeweiligen Ordner.</span><span class="sxs-lookup"><span data-stu-id="c02ef-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="c02ef-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c02ef-175">Examples</span></span>

<span data-ttu-id="c02ef-176">Beispiele für die WHERE-Klausel finden Sie in den Themen zu den einzelnen Prädikaten, die in der obigen Tabelle verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="c02ef-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c02ef-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c02ef-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c02ef-178">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="c02ef-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c02ef-179">Reusewhere-Funktion</span><span class="sxs-lookup"><span data-stu-id="c02ef-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="c02ef-180">Rowset-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c02ef-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="c02ef-181">FROM-Klausel</span><span class="sxs-lookup"><span data-stu-id="c02ef-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="c02ef-182">Übersicht über die SQL-Such Syntax</span><span class="sxs-lookup"><span data-stu-id="c02ef-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="c02ef-183">WITH--as Group Alias-Prädikat</span><span class="sxs-lookup"><span data-stu-id="c02ef-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="c02ef-184">Bereichs-und Verzeichnis Prädikate</span><span class="sxs-lookup"><span data-stu-id="c02ef-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="c02ef-185">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="c02ef-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="c02ef-186">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c02ef-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c02ef-187">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="c02ef-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="c02ef-188">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="c02ef-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



