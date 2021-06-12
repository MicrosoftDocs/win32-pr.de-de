---
description: Erfahren Sie mehr über das SUBQUERY-Argument in Der Windows Shell. Eine Unterabfrage ist eine gespeicherte Suchdatei, die Sie als Filter für eine neue Abfrage verwenden können.
title: SUBQUERY-Argument (Die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010663"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="8aee1-104">SUBQUERY-Argument (Die Windows-Shell)</span><span class="sxs-lookup"><span data-stu-id="8aee1-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="8aee1-105">Eine Unterabfrage ist eine gespeicherte Suchdatei \* (.search-ms), die Sie als Filter für eine neue Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8aee1-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="8aee1-106">Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet.</span><span class="sxs-lookup"><span data-stu-id="8aee1-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="8aee1-107">Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms.</span><span class="sxs-lookup"><span data-stu-id="8aee1-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="8aee1-108">Mithilfe des `subquery` -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.</span><span class="sxs-lookup"><span data-stu-id="8aee1-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="8aee1-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8aee1-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="8aee1-110">Argumentinformationen</span><span class="sxs-lookup"><span data-stu-id="8aee1-110">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="8aee1-111">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="8aee1-111">Minimum Operating System</span></span> | <span data-ttu-id="8aee1-112">Windows Vista mit Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8aee1-112">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



