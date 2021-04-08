---
title: Die type_free_inst-Funktion
description: Die stuften geben den Typ " \_ Free \_ inst" an, um dem dargestellten Typ zugeordneten Arbeitsspeicher freizugeben.
ms.assetid: 4ee2e6a6-b506-445f-adaf-3705228defa7
keywords:
- type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3754106cf8e0cc6e338f91d6c233181aa33038eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856164"
---
# <a name="the-type_free_inst-function"></a><span data-ttu-id="17e85-104">Die \_ typfreie \_ inst-Funktion</span><span class="sxs-lookup"><span data-stu-id="17e85-104">The type\_free\_inst Function</span></span>

<span data-ttu-id="17e85-105">Die stuften **geben den Typ " \_ Free \_ inst** " an, um dem dargestellten Typ zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="17e85-105">The stubs call the **type\_free\_inst** function to free memory associated with the presented type.</span></span> <span data-ttu-id="17e85-106">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="17e85-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="17e85-107">Der-Parameter verweist auf die präsentierte Typinstanz.</span><span class="sxs-lookup"><span data-stu-id="17e85-107">The parameter points to the presented type instance.</span></span> <span data-ttu-id="17e85-108">Dieses Objekt sollte nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17e85-108">This object should not be freed.</span></span> <span data-ttu-id="17e85-109">Eine Erläuterung dazu, wann die-Funktion aufgerufen werden muss, finden Sie unter "über [tragen \_ als](the-transmit-as-attribute.md)"-Attribut.</span><span class="sxs-lookup"><span data-stu-id="17e85-109">For a discussion on when to call the function, see [The transmit\_as Attribute](the-transmit-as-attribute.md).</span></span>

<span data-ttu-id="17e85-110">Im folgenden Beispiel wird die Liste mit doppelten verknüpften freigegeben, indem Sie die Liste bis zum Ende durchlaufen und dann jedes Element der Liste sichern und freigeben.</span><span class="sxs-lookup"><span data-stu-id="17e85-110">In the following example, the double-linked list is freed by walking the list to its end, then backing up and freeing each element of the list.</span></span>


```C++
void __RPC_USER DOUBLE_LINK_TYPE_free_inst(
     DOUBLE_LINK_TYPE __RPC_FAR * pList)
{
    while (pList->pNext != NULL)  // go to end of the list
        pList = pList->pNext;

    pList = pList->pPrevious;
    while (pList != NULL) 
    {  
        // back through the list
        midl_user_free(pList->pNext);
        pList = pList->pPrevious;
    }
} 
```



 

 




