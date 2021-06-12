---
description: Erfahren Sie mehr über das SUBQUERY-Argument in Windows Search. Eine Unterabfrage ist eine gespeicherte Suchdatei, die Sie als Filter für eine neue Abfrage verwenden können.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: SUBQUERY-Argument (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011033"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="1beab-104">SUBQUERY-Argument (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="1beab-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="1beab-105">Eine Unterabfrage ist eine gespeicherte Suchdatei ( .search-ms), die Sie als Filter für \* eine neue Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1beab-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="1beab-106">Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="1beab-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="1beab-107">Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="1beab-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="1beab-108">Mithilfe `subquery` des -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.</span><span class="sxs-lookup"><span data-stu-id="1beab-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="1beab-109">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="1beab-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1beab-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1beab-110">Example</span></span>](#example)
-   [<span data-ttu-id="1beab-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1beab-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="1beab-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1beab-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="1beab-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1beab-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1beab-114">Erste Schritte mit Parameter-Value Argumenten</span><span class="sxs-lookup"><span data-stu-id="1beab-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="1beab-115">Locale Identifier Arguments</span><span class="sxs-lookup"><span data-stu-id="1beab-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="1beab-116">CRUMB-Argument</span><span class="sxs-lookup"><span data-stu-id="1beab-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="1beab-117">SYNTAX-Argument</span><span class="sxs-lookup"><span data-stu-id="1beab-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="1beab-118">STACKEDBY-Argument</span><span class="sxs-lookup"><span data-stu-id="1beab-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



