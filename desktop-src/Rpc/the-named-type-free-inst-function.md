---
title: Die named_type_free_inst-Funktion
description: Die stufstufs nennen die "named \_ Type \_ Free inst"- \_ Funktion, um dem übertragenen Typ zugeordneten Arbeitsspeicher freizugeben.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709090"
---
# <a name="the-named_type_free_inst-function"></a><span data-ttu-id="7d7e5-104">Die benannte \_ \_ typfreie \_ inst-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d7e5-104">The named\_type\_free\_inst Function</span></span>

<span data-ttu-id="7d7e5-105">Die stufstufs nennen die " **Named \_ Type \_ Free \_ inst** "-Funktion, um dem übertragenen Typ zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7d7e5-105">The stubs call the **named\_type\_free\_inst** function to free memory associated with the transmitted type.</span></span> <span data-ttu-id="7d7e5-106">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="7d7e5-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

<span data-ttu-id="7d7e5-107">Der-Parameter verweist auf die Instanz des übertragenen Typs.</span><span class="sxs-lookup"><span data-stu-id="7d7e5-107">The parameter points to the instance of the transmitted type.</span></span> <span data-ttu-id="7d7e5-108">Dieses Objekt sollte nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d7e5-108">This object should not be freed.</span></span> <span data-ttu-id="7d7e5-109">Eine Erläuterung dazu, wann die-Funktion aufgerufen werden muss, finden Sie [unter der Darstellung \_ als-Attribut](the-represent-as-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="7d7e5-109">For a discussion on when to call the function, see [The represent\_as Attribute](the-represent-as-attribute.md).</span></span>

 

 




