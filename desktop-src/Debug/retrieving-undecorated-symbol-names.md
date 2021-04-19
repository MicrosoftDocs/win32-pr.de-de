---
description: Der folgende Code veranschaulicht, wie Sie einen nicht ergänzten Symbolnamen mithilfe von undecoratesymbolname von einem Symbolnamen abrufen können.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Abrufen von nicht ergänzten Symbol Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343015"
---
# <a name="retrieving-undecorated-symbol-names"></a>Abrufen von nicht ergänzten Symbol Namen

Der folgende Code veranschaulicht, wie Sie einen nicht ergänzten Symbolnamen mithilfe von [**undecoratesymbolname**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)von einem Symbolnamen abrufen können. Der ergänzte Name wird in gespeichert `szName` . Im Beispiel wird davon ausgegangen, dass Sie den Symbol Handler initialisiert haben, indem Sie den Code zum [Initialisieren des Symbol Handlers](initializing-the-symbol-handler.md)verwenden.


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



 

 



