---
title: Binden an den Such Start Punkt
description: Der Startpunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält.
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, binden an einen Such Startpunkt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470765"
---
# <a name="binding-to-the-search-start-point"></a><span data-ttu-id="89329-104">Binden an den Such Start Punkt</span><span class="sxs-lookup"><span data-stu-id="89329-104">Binding to the Search Start Point</span></span>

<span data-ttu-id="89329-105">Der Startpunkt für eine Suche ist ein Container, der direkt oder indirekt die gesuchten Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="89329-105">The start point for a search is a container that directly or indirectly contains the objects searched for.</span></span> <span data-ttu-id="89329-106">Die Suche wird in Containern über dem Such Startpunkt nicht durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="89329-106">The search will not be performed in containers above the search start point.</span></span> <span data-ttu-id="89329-107">Nehmen Sie z. b. die folgende hypothetische Verzeichnisstruktur:</span><span class="sxs-lookup"><span data-stu-id="89329-107">For example, take the following hypothetical directory structure:</span></span>

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

<span data-ttu-id="89329-108">Wenn für alle Objekte eine Suche durchgeführt wird und der Such Startpunkt "Container 2" ist, werden nur "Object 3" und "Object 4" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="89329-108">If a search is performed for all objects and the search start point is "Container 2", only "Object 3" and "Object 4" would be retrieved.</span></span> <span data-ttu-id="89329-109">Wenn dieselbe Suche mit dem Such Startpunkt bei "Container 1" durchgeführt wurde, werden "Objekt 1" und "Objekt 2" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="89329-109">If the same search was performed with the search start point at "Container 1", "Object 1" and "Object 2" would be retrieved.</span></span>

<span data-ttu-id="89329-110">Binden Sie zum Binden an den Such Startpunkt an den ADsPath des Containers, der als Such Startpunkt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89329-110">To bind to the search start point, bind to the ADsPath of the container that will be the search start point.</span></span>

 

 




