---
description: Das Freitext-Prädikat ist Teil der WHERE-Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Frei Text Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750385"
---
# <a name="freetext-predicate"></a><span data-ttu-id="1f379-103">Frei Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="1f379-103">FREETEXT Predicate</span></span>

<span data-ttu-id="1f379-104">Das Freitext-Prädikat ist Teil der [Where](-search-sql-where.md) -Klausel und unterstützt das Suchen nach Wörtern und Ausdrücken in Textspalten.</span><span class="sxs-lookup"><span data-stu-id="1f379-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="1f379-105">Verwenden Sie das frei Text Prädikat, um Dokumente zu suchen, die Kombinationen der Suchwörter enthalten, die in den angegebenen Inhalten oder Spalten verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="1f379-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="1f379-106">Um den Rangwert zu erhalten, schließen Sie "System. search. Rank" ein, bei dem es sich um eine Rangfolge der Relevanz handelt, als eine Spalte in der SELECT-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="1f379-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="1f379-107">Das Freitext-Prädikat weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="1f379-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="1f379-108">Der voll Textspalten Verweis ist optional.</span><span class="sxs-lookup"><span data-stu-id="1f379-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="1f379-109">Damit können Sie eine einzelne Spalte oder einen [Spalten Gruppierungs Alias](-search-sql-with-as.md) angeben, für den das Freitext Prädikat getestet wird.</span><span class="sxs-lookup"><span data-stu-id="1f379-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="1f379-110">Wenn die voll Text Spalte als "All" oder "" angegeben wird \* , werden alle indizierten Texteigenschaften durchsucht.</span><span class="sxs-lookup"><span data-stu-id="1f379-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="1f379-111">Obwohl es sich bei der Spalte nicht um eine Text Eigenschaft handeln muss, können die Ergebnisse bedeutungslos sein, wenn es sich bei der Spalte um einen anderen Datentyp handelt.</span><span class="sxs-lookup"><span data-stu-id="1f379-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="1f379-112">Der Spaltenname kann entweder ein regulärer oder ein Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein, und Sie müssen ihn durch ein Komma von der Bedingung trennen.</span><span class="sxs-lookup"><span data-stu-id="1f379-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="1f379-113">Wenn keine voll Text Bedingung angegeben wird, wird die Inhaltsspalte verwendet, die den Hauptteil des Dokuments ist.</span><span class="sxs-lookup"><span data-stu-id="1f379-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="1f379-114">Sie können ein Suchgebiets Schema angeben, um die entsprechende Wörter Trennung und die Flexions Formen für die Suchabfrage zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1f379-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="1f379-115">Gültige Gebiets Schema Werte sind ein Windows-Standard Sprachcode Bezeichner (LCID).</span><span class="sxs-lookup"><span data-stu-id="1f379-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="1f379-116">Beispielsweise ist 1033 die LCID für USA-Englisch.</span><span class="sxs-lookup"><span data-stu-id="1f379-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="1f379-117">Platzieren Sie die LCID als letztes Element innerhalb der Klammern der Freitext-Klausel.</span><span class="sxs-lookup"><span data-stu-id="1f379-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="1f379-118">Wichtige Informationen zum Suchen von und Sprachen finden [Sie unter Verwenden lokalisierter Such](-search-sql-usinglocsearches.md)Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1f379-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="1f379-119">Das Standard Gebiets Schema für die Suche ist das Standard Gebiets Schema des Systems.</span><span class="sxs-lookup"><span data-stu-id="1f379-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="1f379-120">Sie müssen den Bereich für die Freitext Bedingung in einfache Anführungszeichen einschließen, und er muss aus mindestens einem Suchbegriff bestehen.</span><span class="sxs-lookup"><span data-stu-id="1f379-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="1f379-121">Das Freitext Prädikat unterstützt keine logischen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="1f379-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="1f379-122">Um nach einem Ausdruck zu suchen, als ob es sich um ein einzelnes Wort handelt, schließen Sie den Ausdruck in doppelte Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="1f379-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="1f379-123">Wenn Sie das frei Text Prädikat verwenden, geben die Suchabfrage Ergebnisse Dokumente zurück, die alle Suchbegriffe enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f379-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="1f379-124">Die Begriffe müssen nicht in einer bestimmten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f379-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="1f379-125">Dokumente, die mehr Suchbegriffe enthalten, weisen Spaltenwerte höherer Rangfolge auf.</span><span class="sxs-lookup"><span data-stu-id="1f379-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="1f379-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f379-126">Examples</span></span>

<span data-ttu-id="1f379-127">Im folgenden Beispiel wird nach Dokumenten gesucht, die "Computer", "Software", "Hardware" oder Kombinationen aus diesen Wörtern enthalten:</span><span class="sxs-lookup"><span data-stu-id="1f379-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="1f379-128">Es ist nicht möglich, eine einzelne Wort Abgleich und einen übereinstimmenden Ausdruck in demselben Freitext Prädikat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f379-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="1f379-129">Beim Ausführen von Abfragen mit kontra Zuwendungen müssen Sie das Anführungszeichen bei der Verwendung von frei Text mit Escapezeichen versehen, jedoch nicht, wenn Sie enthält.</span><span class="sxs-lookup"><span data-stu-id="1f379-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="1f379-130">Beispielsweise kann die folgende Syntax nicht ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="1f379-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="1f379-131">Die korrekte Syntax umfasst zwei einfache Anführungszeichen, nicht ein doppeltes Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="1f379-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="1f379-132">Die folgende Syntax ist erfolgreich:</span><span class="sxs-lookup"><span data-stu-id="1f379-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="1f379-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1f379-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1f379-134">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="1f379-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f379-135">Enthält Prädikat</span><span class="sxs-lookup"><span data-stu-id="1f379-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="1f379-136">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="1f379-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="1f379-137">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1f379-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f379-138">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="1f379-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



