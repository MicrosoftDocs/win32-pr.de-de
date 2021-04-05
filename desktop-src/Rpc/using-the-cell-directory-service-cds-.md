---
title: Verwenden des Zellen Verzeichnis Dienstanbieter (CDs)
description: Wenn Sie CDs haben, können Sie diese anstelle von Microsoft Locator verwenden.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Remote Prozedur Aufruf RPC, Tasks, verwenden des Zellen Verzeichnis Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710583"
---
# <a name="using-the-cell-directory-service-cds"></a><span data-ttu-id="88133-104">Verwenden des Zellen Verzeichnis Dienstanbieter (CDs)</span><span class="sxs-lookup"><span data-stu-id="88133-104">Using the Cell Directory Service (CDS)</span></span>

<span data-ttu-id="88133-105">Wenn Sie CDs haben, können Sie diese anstelle von Microsoft Locator verwenden.</span><span class="sxs-lookup"><span data-stu-id="88133-105">If you have CDS, you can use it instead of Microsoft Locator.</span></span> <span data-ttu-id="88133-106">Ändern Sie die Registrierungseinträge wie gezeigt:</span><span class="sxs-lookup"><span data-stu-id="88133-106">Change the registry entries as shown:</span></span>

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

<span data-ttu-id="88133-107">Das Ändern dieser Einträge verweist auf einen Gatewaycomputer, auf dem die nsid ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88133-107">Changing these entries will point to a gateway computer that is running the NSID.</span></span> <span data-ttu-id="88133-108">Diese wird als hauptlocator verwendet.</span><span class="sxs-lookup"><span data-stu-id="88133-108">This will be used as the master locator.</span></span> <span data-ttu-id="88133-109">Bei einem Absturz wird keine Suche nach einem Ersatz durchsucht.</span><span class="sxs-lookup"><span data-stu-id="88133-109">In the event of a crash, there will be no search for a replacement.</span></span>

 

 




