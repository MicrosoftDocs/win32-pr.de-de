---
description: Der Windows Search-Structured Query Language (SQL) ähnelt einer SQL-Standard Abfrage.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Übersicht über die SQL-Syntax von Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041629"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="3de4c-103">Übersicht über die SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="3de4c-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="3de4c-104">Der Windows Search-Structured Query Language (SQL) ähnelt einer SQL-Standard Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3de4c-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="3de4c-105">Dies wird in den folgenden beiden Syntaxen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="3de4c-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="3de4c-106">Im folgenden Abfrage Beispiel werden die Werte für die Seitenanzahl und den Erstellungsdatum für alle Dokumente zurückgegeben, die mehr als 50 Seiten enthalten, sortiert ist die aufsteigende Reihenfolge der Seitenanzahl.</span><span class="sxs-lookup"><span data-stu-id="3de4c-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="3de4c-107">Die Syntax der Windows-Suchabfrage unterstützt viele Optionen und ermöglicht so kompliziertere Abfragen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="3de4c-108">In der folgenden Tabelle werden die einzelnen-Klauseln in der SELECT-oder Group on-Anweisung und die unterstützten Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3de4c-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="3de4c-109">Klausel</span><span class="sxs-lookup"><span data-stu-id="3de4c-109">Clause</span></span>                                              | <span data-ttu-id="3de4c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3de4c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3de4c-111">Gruppieren nach... Über...</span><span class="sxs-lookup"><span data-stu-id="3de4c-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="3de4c-112">Gibt an, wie die von der Abfrage zurückgegebenen Ergebnisse gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="3de4c-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="3de4c-113">Sie können die Bereiche angeben, nach denen gruppiert werden soll, und mehr als eine Spalte für die Gruppierung angeben.</span><span class="sxs-lookup"><span data-stu-id="3de4c-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="3de4c-114">Beispielsweise können Sie Ergebnisse in einem Bereich von Dateigrößen gruppieren (Größe < 100, 100 <= Größe < 1000; 1000 <= Größe) und Schachteln von Gruppierungen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="3de4c-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="3de4c-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="3de4c-116">Gibt die von der Abfrage zurückgegebenen Spalten an.</span><span class="sxs-lookup"><span data-stu-id="3de4c-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3de4c-117">FROM</span><span class="sxs-lookup"><span data-stu-id="3de4c-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="3de4c-118">Gibt den zu durchsuchenden Computer und Katalog an.</span><span class="sxs-lookup"><span data-stu-id="3de4c-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3de4c-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="3de4c-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="3de4c-120">Gibt an, was ein entsprechendes Dokument ausmacht.</span><span class="sxs-lookup"><span data-stu-id="3de4c-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="3de4c-121">Diese Klausel verfügt über viele Optionen und ermöglicht eine umfassende Kontrolle über die Suchbedingungen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="3de4c-122">Beispielsweise können Sie mit Wörtern, Ausdrücken, flektiven Wort Formularen, Zeichen folgen, numerischen und bitweisen Werten und mehrwertigen Arrays vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3de4c-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="3de4c-123">Sie können auch statistische Gewichtungen auf die übereinstimmenden Bedingungen anwenden und übereinstimmende Bedingungen mit booleschen Operatoren kombinieren.</span><span class="sxs-lookup"><span data-stu-id="3de4c-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="3de4c-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="3de4c-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="3de4c-125">Gibt die Sortierreihenfolge für die von der Abfrage zurückgegebenen Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="3de4c-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="3de4c-126">Sie können mehr als ein Feld angeben, in dem die Ergebnisse sortiert werden, und Sie können aufsteigende oder absteigende Reihenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="3de4c-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="3de4c-127">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="3de4c-127">Code samples</span></span>

<span data-ttu-id="3de4c-128">Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über SQL.</span><span class="sxs-lookup"><span data-stu-id="3de4c-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="3de4c-129">Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3de4c-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="3de4c-130">Beide Beispiele sind auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3de4c-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3de4c-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3de4c-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="3de4c-132">Referenz</span><span class="sxs-lookup"><span data-stu-id="3de4c-132">Reference</span></span>

[<span data-ttu-id="3de4c-133">Literale</span><span class="sxs-lookup"><span data-stu-id="3de4c-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="3de4c-134">Verwenden lokalisierter Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="3de4c-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="3de4c-135">Verstehen von relevanzwerten</span><span class="sxs-lookup"><span data-stu-id="3de4c-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="3de4c-136">Eigenschafts Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="3de4c-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="3de4c-137">Erweiterte Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="3de4c-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="3de4c-138">Konzept</span><span class="sxs-lookup"><span data-stu-id="3de4c-138">Conceptual</span></span>

[<span data-ttu-id="3de4c-139">SQL-Erweiterungen in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="3de4c-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="3de4c-140">SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3de4c-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="3de4c-141">Identifiers (Bezeichner)</span><span class="sxs-lookup"><span data-stu-id="3de4c-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="3de4c-142">Groß-/Kleinschreibung in suchen</span><span class="sxs-lookup"><span data-stu-id="3de4c-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="3de4c-143">Diakritische Empfindlichkeit bei Such Vorgängen</span><span class="sxs-lookup"><span data-stu-id="3de4c-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="3de4c-144">Umwandeln des Datentyps einer Spalte</span><span class="sxs-lookup"><span data-stu-id="3de4c-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="3de4c-145">Datentypzuordnungen</span><span class="sxs-lookup"><span data-stu-id="3de4c-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
