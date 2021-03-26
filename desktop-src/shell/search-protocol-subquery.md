---
description: Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.
title: Unterabfrage Argument (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995038"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="b477c-103">Unterabfrage Argument (die Windows-Shell)</span><span class="sxs-lookup"><span data-stu-id="b477c-103">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="b477c-104">Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b477c-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="b477c-105">Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="b477c-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="b477c-106">Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage durch eine e-Mail-Verteilerliste einschränken: myDepartment. Search-MS, teamproject. Search-MS und corporatewide. Search-ms.</span><span class="sxs-lookup"><span data-stu-id="b477c-106">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="b477c-107">Mit dem `subquery` -Argument können Sie e-Mail-Suchvorgänge auf beliebige oder alle dieser gespeicherten Suchvorgänge beschränken.</span><span class="sxs-lookup"><span data-stu-id="b477c-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="b477c-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b477c-108">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="b477c-109">Argument Informationen</span><span class="sxs-lookup"><span data-stu-id="b477c-109">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="b477c-110">Mindestens Betriebs System</span><span class="sxs-lookup"><span data-stu-id="b477c-110">Minimum Operating System</span></span> | <span data-ttu-id="b477c-111">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b477c-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



