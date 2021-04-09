---
title: Nur Attribute suchen
description: Manchmal führen Sie eine Suche durch, um zu ermitteln, welche Art von Daten für ein Objekt verfügbar ist.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Nur Attribute suchen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947331"
---
# <a name="search-attributes-only"></a><span data-ttu-id="b4373-104">Nur Attribute suchen</span><span class="sxs-lookup"><span data-stu-id="b4373-104">Search Attributes Only</span></span>

<span data-ttu-id="b4373-105">Manchmal führen Sie eine Suche durch, um zu ermitteln, welche Art von Daten für ein Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b4373-105">Sometimes you perform a search to determine what type of data is available for an object.</span></span> <span data-ttu-id="b4373-106">In diesem Fall interessieren Sie sich nur für die Attribute und nicht für die Werte des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b4373-106">In this case, you are interested only in the attributes, and not the values, of the object.</span></span> <span data-ttu-id="b4373-107">Um dies zu erreichen, legen Sie die Option "nur Attribute suchen" fest.</span><span class="sxs-lookup"><span data-stu-id="b4373-107">To accomplish this, you set the "search attributes only" option.</span></span> <span data-ttu-id="b4373-108">Wenn Sie diese Option angeben, werden die Attributnamen ohne ihre Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b4373-108">Specifying this option returns the attribute names without their values.</span></span> <span data-ttu-id="b4373-109">Das Resultset enthält jedoch nur die Attribute, denen Werte zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b4373-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="b4373-110">Nehmen Sie beispielsweise ein Objekt mit den folgenden Attributen:</span><span class="sxs-lookup"><span data-stu-id="b4373-110">For example, consider an object with the following attributes:</span></span>

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

<span data-ttu-id="b4373-111">Wenn die Option nur Such Attribute festgelegt ist, enthält das Resultset Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b4373-111">When the search attributes only option is set, the result set includes:</span></span>

``` syntax
First Name
Last Name
Phone Number
```

<span data-ttu-id="b4373-112">Weitere Informationen zum Verwenden der Option nur Such Attribute mit einer bestimmten Suchschnittstelle finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="b4373-112">For more information about using the search attributes only option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="b4373-113">Zurückgeben von Attributnamen mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="b4373-113">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)
-   [<span data-ttu-id="b4373-114">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="b4373-114">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="b4373-115">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="b4373-115">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




