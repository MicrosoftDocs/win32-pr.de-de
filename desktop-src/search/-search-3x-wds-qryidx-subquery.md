---
description: Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Unterabfrage Argument (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958785"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="45968-103">Unterabfrage Argument (Windows-Suche)</span><span class="sxs-lookup"><span data-stu-id="45968-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="45968-104">Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="45968-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="45968-105">Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="45968-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="45968-106">Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage durch eine e-Mail-Verteilerliste einschränken: myDepartment. Search-MS, teamproject. Search-MS und corporatewide. Search-ms.</span><span class="sxs-lookup"><span data-stu-id="45968-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="45968-107">Mit dem `subquery` -Argument können Sie e-Mail-Suchvorgänge auf beliebige oder alle dieser gespeicherten Suchvorgänge beschränken.</span><span class="sxs-lookup"><span data-stu-id="45968-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="45968-108">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="45968-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="45968-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45968-109">Example</span></span>](#example)
-   [<span data-ttu-id="45968-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45968-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="45968-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45968-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="45968-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45968-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45968-113">Die ersten Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="45968-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="45968-114">Locale-bezeichnerargumente</span><span class="sxs-lookup"><span data-stu-id="45968-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="45968-115">Crumb-Argument</span><span class="sxs-lookup"><span data-stu-id="45968-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="45968-116">Syntax Argument</span><span class="sxs-lookup"><span data-stu-id="45968-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="45968-117">Stackedby-Argument</span><span class="sxs-lookup"><span data-stu-id="45968-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



