---
description: Erfahren Sie mehr über das SUBQUERY-Argument in The Windows Shell. Eine Unterabfrage ist eine gespeicherte Suchdatei, die Sie als Filter für eine neue Abfrage verwenden können.
title: SUBQUERY-Argument (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581598"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="512b3-104">SUBQUERY-Argument (die Windows Shell)</span><span class="sxs-lookup"><span data-stu-id="512b3-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="512b3-105">Eine Unterabfrage ist eine gespeicherte Suchdatei \* (.search-ms), die Sie als Filter für eine neue Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="512b3-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="512b3-106">Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="512b3-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="512b3-107">Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="512b3-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="512b3-108">Mithilfe des `subquery` -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.</span><span class="sxs-lookup"><span data-stu-id="512b3-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="512b3-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="512b3-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="512b3-110">Argumentinformationen</span><span class="sxs-lookup"><span data-stu-id="512b3-110">Argument Information</span></span>



|                              | <span data-ttu-id="512b3-111">Wert</span><span class="sxs-lookup"><span data-stu-id="512b3-111">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="512b3-112">**Mindestbetriebssystem**</span><span class="sxs-lookup"><span data-stu-id="512b3-112">**Minimum Operating System**</span></span> | <span data-ttu-id="512b3-113">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="512b3-113">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



