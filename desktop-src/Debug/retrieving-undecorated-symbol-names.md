---
description: Der folgende Code veranschaulicht das Abrufen eines nicht korrigierten Symbolnamens aus einem Symbolnamen mit unDecorateSymbolName.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Abrufen von nicht korrigierten Symbolnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076344"
---
# <a name="retrieving-undecorated-symbol-names"></a>Abrufen von nicht korrigierten Symbolnamen

Der folgende Code veranschaulicht, wie ein nicht korrigierter Symbolname mithilfe von [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)aus einem Symbolnamen abgerufen wird. Der ergänzte Name wird in `szName` gespeichert. Im Beispiel wird davon ausgegangen, dass Sie den Symbolhandler mithilfe des Codes in [Initialisieren des Symbolhandlers initialisiert](initializing-the-symbol-handler.md)haben.


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



