---
title: Die type_free_xmit-Funktion
description: Die Stubdateien nennen die Type \_ Free \_ xmit-Funktion, um Speicher freizugeben, der den übertragenen Daten zugeordnet ist.
ms.assetid: f15ce25b-d36c-4ee5-b796-f0aba1997047
keywords:
- type_free_xmit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33d5cb8079d50923de2161b0384550829a5f22f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206837"
---
# <a name="the-type_free_xmit-function"></a><span data-ttu-id="36225-104">Die Type \_ Free \_ xmit-Funktion</span><span class="sxs-lookup"><span data-stu-id="36225-104">The type\_free\_xmit Function</span></span>

<span data-ttu-id="36225-105">Die Stubdateien nennen die **Type \_ Free \_ xmit** -Funktion, um Speicher freizugeben, der den übertragenen Daten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36225-105">The stubs call the **type\_free\_xmit** function to free memory associated with the transmitted data.</span></span> <span data-ttu-id="36225-106">Nachdem der [Typ \_ aus der \_ xmit](the-type-from-xmit-function.md) -Funktion die übertragenen Daten in den dargestellten Typ konvertiert hat, wird der Arbeitsspeicher nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="36225-106">After the [type\_from\_xmit](the-type-from-xmit-function.md) function converts the transmitted data to its presented type, the memory is no longer needed.</span></span> <span data-ttu-id="36225-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="36225-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <type>_free_xmit(<xmit_type> __RPC_FAR *);
```

<span data-ttu-id="36225-108">Der-Parameter ist ein Zeiger auf den Arbeitsspeicher, in dem der übertragene Typ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="36225-108">The parameter is a pointer to the memory that contains the transmitted type.</span></span>

<span data-ttu-id="36225-109">In diesem Beispiel enthält der Arbeitsspeicher ein Array, das sich in einer einzelnen Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="36225-109">In this example, the memory contains an array that is in a single structure.</span></span> <span data-ttu-id="36225-110">Die Funktion "Double \_ Link \_ Type \_ Free \_ xmit" verwendet die vom Benutzer bereitgestellte Funktion "Mittel l \_ Benutzer frei" \_ , um den Arbeitsspeicher freizugeben:</span><span class="sxs-lookup"><span data-stu-id="36225-110">The function DOUBLE\_LINK\_TYPE\_free\_xmit uses the user-supplied function midl\_user\_free to free the memory:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_free_xmit( 
     DOUBLE_XMIT_TYPE __RPC_FAR * pArray)
{
     midl_user_free(pArray);
}
```

 

 




