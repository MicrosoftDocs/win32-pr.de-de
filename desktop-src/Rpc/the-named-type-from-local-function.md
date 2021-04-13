---
title: Die named_type_from_local-Funktion
description: Die stubzeichen nennen den benannten \_ Typ \_ von der \_ lokalen Funktion.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309603"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="4dbfc-104">Der benannte \_ Typ \_ aus der \_ lokalen Funktion.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="4dbfc-105">Die stubzeichen nennen den benannten \_ Typ \_ von der \_ lokalen Funktion.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="4dbfc-106">Der Typ, der von der Anwendung verwendet wird, wird in den Typ konvertiert, den die stusb über das Netzwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="4dbfc-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4dbfc-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="4dbfc-108">Der erste Parameter ist ein Zeiger auf die Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="4dbfc-109">Der zweite Parameter ist ein Zeiger auf einen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="4dbfc-110">Die Funktion verweist auf die übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="4dbfc-111">Die Funktion muss Arbeitsspeicher für den übertragenen Typ zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4dbfc-111">The function must allocate memory for the transmitted type.</span></span>

 

 




