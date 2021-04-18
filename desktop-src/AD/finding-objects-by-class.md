---
title: Suchen nach Objekten nach Klasse
description: Eine typische Suchabfrage für eine bestimmte Objektklasse.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Suchen nach Objekten nach Klasse AD
- Active Directory, verwenden, suchen, nach Klasse
- Objekt-AD, Suche nach Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337754"
---
# <a name="finding-objects-by-class"></a><span data-ttu-id="72cf1-106">Suchen nach Objekten nach Klasse</span><span class="sxs-lookup"><span data-stu-id="72cf1-106">Finding Objects by Class</span></span>

<span data-ttu-id="72cf1-107">Eine typische Suchabfrage für eine bestimmte Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="72cf1-107">A typical search queries for a specific object class.</span></span> <span data-ttu-id="72cf1-108">Im folgenden Codebeispiel wird nach Computern mit dem Standort in der Gebäude 7N gesucht.</span><span class="sxs-lookup"><span data-stu-id="72cf1-108">The following code example searches for computers with location in Building 7N.</span></span>


```C++
(&(objectCategory=computer)(location=Building 7N))
```



<span data-ttu-id="72cf1-109">Bedenken Sie, warum **objectClass** nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72cf1-109">Consider why **objectClass** is not used.</span></span> <span data-ttu-id="72cf1-110">Verwenden Sie **objectClass** nicht ohne einen anderen Vergleich, der ein indiziertes Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="72cf1-110">Do not use **objectClass** without another comparison that contains an indexed attribute.</span></span> <span data-ttu-id="72cf1-111">Index Attribute können die Effizienz einer Abfrage erhöhen.</span><span class="sxs-lookup"><span data-stu-id="72cf1-111">Index attributes can increase the efficiency of a query.</span></span> <span data-ttu-id="72cf1-112">Das **objectClass** -Attribut ist mehr wertig und nicht indiziert.</span><span class="sxs-lookup"><span data-stu-id="72cf1-112">The **objectClass** attribute is multi-valued and not indexed.</span></span> <span data-ttu-id="72cf1-113">Verwenden Sie **objectCategory**, um den Typ oder die Klasse eines Objekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="72cf1-113">To specify the type or class of an object, use **objectCategory**.</span></span>

<span data-ttu-id="72cf1-114">Weniger effizient:</span><span class="sxs-lookup"><span data-stu-id="72cf1-114">Less efficient:</span></span>


```C++
(objectClass=computer)
```



<span data-ttu-id="72cf1-115">Effizienter:</span><span class="sxs-lookup"><span data-stu-id="72cf1-115">More Efficient:</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="72cf1-116">Beachten Sie, dass es einige Fälle gibt, in denen eine Kombination aus " **objectClass** " und " **objectCategory** " verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="72cf1-116">Be aware that there are some cases where a combination of **objectClass** and **objectCategory** must be used.</span></span> <span data-ttu-id="72cf1-117">Die User-Klasse und die Contact-Klasse sollten wie folgt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72cf1-117">The user class and contact class should be specified as follows.</span></span>


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



<span data-ttu-id="72cf1-118">Beachten Sie, dass Sie mit den folgenden Benutzern und Kontakten nach Benutzern und Kontakten suchen können.</span><span class="sxs-lookup"><span data-stu-id="72cf1-118">Be aware that you could search for both users and contacts with the following.</span></span>


```C++
(objectCategory=person)
```



 

 




