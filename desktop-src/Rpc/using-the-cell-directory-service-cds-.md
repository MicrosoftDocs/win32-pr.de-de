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
# <a name="using-the-cell-directory-service-cds"></a>Verwenden des Zellen Verzeichnis Dienstanbieter (CDs)

Wenn Sie CDs haben, können Sie diese anstelle von Microsoft Locator verwenden. Ändern Sie die Registrierungseinträge wie gezeigt:

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

Das Ändern dieser Einträge verweist auf einen Gatewaycomputer, auf dem die nsid ausgeführt wird. Diese wird als hauptlocator verwendet. Bei einem Absturz wird keine Suche nach einem Ersatz durchsucht.

 

 




