---
title: Verwenden des Cell Directory Service (CDS)
description: Wenn Sie über CDS verfügen, können Sie es anstelle von Microsoft Locator verwenden.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Remoteprozeduraufruf RPC , Tasks mithilfe des Zellenverzeichnisdiensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010637"
---
# <a name="using-the-cell-directory-service-cds"></a>Verwenden des Cell Directory Service (CDS)

Wenn Sie über CDS verfügen, können Sie es anstelle von Microsoft Locator verwenden. Ändern Sie die Registrierungseinträge wie gezeigt:

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

Das Ändern dieser Einträge wird auf einen Gatewaycomputer zeigen, auf dem die NSID ausgeführt wird. Dieser wird als Masterlocator verwendet. Bei einem Absturz wird nicht nach einem Ersatz gesucht.

 

 




