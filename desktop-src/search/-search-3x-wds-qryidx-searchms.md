---
description: Das Search-MS-Anwendungsprotokoll ist eine Konvention zum Abfragen des Windows-Suchindex.
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: Abfragen des Indexes mit dem Search-MS-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750417"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="e9456-103">Abfragen des Indexes mit dem Search-MS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e9456-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="e9456-104">Das **Search-MS-**  [Anwendungsprotokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine Konvention zum Abfragen des Windows-Suchindex.</span><span class="sxs-lookup"><span data-stu-id="e9456-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="e9456-105">Das Protokoll ermöglicht Anwendungen wie Windows-Explorer, den Index mit Parameter-Wert-Argumenten abzufragen, einschließlich Eigenschafts Argumenten, zuvor gespeicherter Suchvorgänge, erweiterter Abfrage Syntax (AQS), natürlicher Abfrage Syntax (NQS) und Sprachcode Bezeichner (LCIDs) für den Indexer und die Abfrage selbst.</span><span class="sxs-lookup"><span data-stu-id="e9456-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="e9456-106">Dieser Abschnitt ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="e9456-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="e9456-107">Die ersten Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="e9456-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="e9456-108">Locale-bezeichnerargumente</span><span class="sxs-lookup"><span data-stu-id="e9456-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="e9456-109">Crumb-Argument</span><span class="sxs-lookup"><span data-stu-id="e9456-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="e9456-110">Syntax Argument</span><span class="sxs-lookup"><span data-stu-id="e9456-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="e9456-111">Stackedby-Argument</span><span class="sxs-lookup"><span data-stu-id="e9456-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="e9456-112">Unterabfrage Argument</span><span class="sxs-lookup"><span data-stu-id="e9456-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="e9456-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9456-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9456-114">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="e9456-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e9456-115">Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="e9456-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e9456-116">Abfragen des Indexes mit isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="e9456-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="e9456-117">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="e9456-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="e9456-118">Programm gesteuertes verwenden der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="e9456-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
