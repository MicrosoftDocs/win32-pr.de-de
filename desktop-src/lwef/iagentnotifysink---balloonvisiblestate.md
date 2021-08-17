---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f61f1213c6d947f2ca23e0b67ff8eef393892f4732e4a419ec93c277a62af99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976180"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>IAgentNotifySink::BalloonVisibleState

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Benachrichtigt eine Clientanwendung, wenn sich der Sichtbarkeitszustand des Wortsprechblasenworts des Zeichens ändert.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des Zeichens, dessen Sichtbarkeitszustand des Wortsprechblasens geändert wurde.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Sichtbarkeitsflag. Dieser boolesche Wert ist **True,** wenn die Wortsprechblase des Zeichens sichtbar wird. und **FALSE,** wenn es ausgeblendet wird.

</dd> </dl>

Dieses Ereignis wird an alle Clients des Zeichens gesendet.

 

 




