---
title: Die named_type_free_local-Funktion
description: Der stubspeicher Ruft den Typ " \_ freie \_ lokale Funktion" auf, um den von einem Aufrufen des benannten Typs zugeordneten Arbeitsspeicher \_ für die \_ \_ lokale Routine freizugeben.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709089"
---
# <a name="the-named_type_free_local-function"></a><span data-ttu-id="07d72-104">Die benannte \_ \_ typfreie \_ lokale Funktion</span><span class="sxs-lookup"><span data-stu-id="07d72-104">The named\_type\_free\_local Function</span></span>

<span data-ttu-id="07d72-105">Der stubspeicher Ruft den **Typ " \_ freie \_ lokale** Funktion" auf, um den von einem Aufrufen des benannten Typs zugeordneten Arbeitsspeicher [ \_ für die \_ \_ lokale](the-named-type-to-local-function.md) Routine freizugeben.</span><span class="sxs-lookup"><span data-stu-id="07d72-105">The stubs call the **type\_free\_local** function to free the memory allocated by a call to the [named\_type\_to\_local](the-named-type-to-local-function.md) routine.</span></span> <span data-ttu-id="07d72-106">Der vom Stub zugeordnete Arbeitsspeicher wird nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="07d72-106">It does not free the memory allocated by the stub.</span></span> <span data-ttu-id="07d72-107">Der Funktionsprototyp wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="07d72-107">The function prototype is defined as:</span></span>

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

<span data-ttu-id="07d72-108">Der-Parameter ist ein Zeiger auf den Arbeitsspeicher **, der vom benannten \_ Typ \_ zu \_ local** zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="07d72-108">The parameter is a pointer to the memory allocated by **named\_type\_to\_local**.</span></span>

 

 




