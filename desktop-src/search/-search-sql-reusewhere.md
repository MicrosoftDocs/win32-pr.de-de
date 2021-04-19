---
description: Die WHERE-Klausel in einer Abfrage gibt eine Menge von Elementen an, mit denen die Ergebnisse verglichen werden sollen.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Reusewhere-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353025"
---
# <a name="reusewhere-function"></a><span data-ttu-id="c700d-103">Reusewhere-Funktion</span><span class="sxs-lookup"><span data-stu-id="c700d-103">ReuseWhere Function</span></span>

<span data-ttu-id="c700d-104">Die [Where](-search-sql-where.md) -Klausel in einer Abfrage gibt eine Menge von Elementen an, mit denen die Ergebnisse verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c700d-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="c700d-105">Nachfolgende Abfragen können die Arbeit, die für eine vorherige Abfrage ausgeführt wird, mithilfe der reusewhere-Funktion in einer neuen Abfrage in der WHERE-Klausel freigeben.</span><span class="sxs-lookup"><span data-stu-id="c700d-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="c700d-106">Abfragen, die diese Funktion nutzen, werden schneller ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c700d-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="c700d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c700d-107">Examples</span></span>

<span data-ttu-id="c700d-108">Im folgenden Szenario wird gezeigt, wie die reusewhere-Funktion verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="c700d-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="c700d-109">Sie geben die folgende Abfrage aus:</span><span class="sxs-lookup"><span data-stu-id="c700d-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="c700d-110">Aus dem zurückgegebenen Rowset erhalten Sie eine [Where-ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="c700d-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="c700d-111">Die WHERE-ID ist eine Rowseteigenschaft mit dem propset {aa6ee6b0-E828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 und Type UI4.</span><span class="sxs-lookup"><span data-stu-id="c700d-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="c700d-112">Sie geben eine zweite Abfrage mit der reusewhere-Funktion aus und übergeben dabei den *Query1WhereID* aus Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="c700d-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="c700d-113">Die zweite Abfrage entspricht Folgendem:</span><span class="sxs-lookup"><span data-stu-id="c700d-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="c700d-114">Die reusewhere-Funktion kann in der [Where](-search-sql-where.md) -Klausel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c700d-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c700d-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c700d-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c700d-116">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="c700d-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c700d-117">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="c700d-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="c700d-118">Rowset-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c700d-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



