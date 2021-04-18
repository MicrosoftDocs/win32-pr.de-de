---
description: Die Microsoft Windows Search-Abfragesprache unterstützt sechs Prädikate, die keine Volltextsuche sind. Die in diesem Abschnitt beschriebenen Prädikate sind in der folgenden Tabelle aufgeführt.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Nicht-voll Text Prädikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344264"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="4b0e2-104">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="4b0e2-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="4b0e2-105">Die Microsoft Windows Search-Abfragesprache unterstützt sechs Prädikate, die keine Volltextsuche sind.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="4b0e2-106">Die in diesem Abschnitt beschriebenen Prädikate sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="4b0e2-107">Nicht-voll Text Prädikat</span><span class="sxs-lookup"><span data-stu-id="4b0e2-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="4b0e2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b0e2-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b0e2-109">Alle bitweisen und einige bitweise</span><span class="sxs-lookup"><span data-stu-id="4b0e2-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="4b0e2-110">Ein Satz von Schlüsselwörtern, bei denen die Bits in einem ganzzahligen Typ getestet werden.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="4b0e2-111">DateAdd-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b0e2-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="4b0e2-112">Führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="4b0e2-113">Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="4b0e2-114">LIKE-Prädikat</span><span class="sxs-lookup"><span data-stu-id="4b0e2-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="4b0e2-115">Vergleicht Spaltenwerte mithilfe eines einfachen Musterabgleich mit Platzhalter Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="4b0e2-116">Vergleich von literalen Werten</span><span class="sxs-lookup"><span data-stu-id="4b0e2-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="4b0e2-117">Vergleicht Spaltenwerte mit Zeichen folgen-, Datums-, Zeitstempel-, numerischen und anderen Literalwerten.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="4b0e2-118">Dieses Prädikat unterstützt Ungleichheiten wie "größer als" (">") und "kleiner als" ("<").</span><span class="sxs-lookup"><span data-stu-id="4b0e2-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="4b0e2-119">Mehrwertige Vergleiche (Array)</span><span class="sxs-lookup"><span data-stu-id="4b0e2-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="4b0e2-120">Vergleicht mehrwertige Spalten mit einem mehrwertigen Array von Literalen.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="4b0e2-121">NULL-Prädikat</span><span class="sxs-lookup"><span data-stu-id="4b0e2-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="4b0e2-122">Erkennt Spaltenwerte, die für das Dokument nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="4b0e2-123">Such Abfragen mit dem **null** -Prädikat können erfordern, dass die Windows-Suche den gesamten Katalog scannt, was die Leistung der Abfrage verlangsamen könnte.</span><span class="sxs-lookup"><span data-stu-id="4b0e2-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4b0e2-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b0e2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0e2-125">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="4b0e2-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



