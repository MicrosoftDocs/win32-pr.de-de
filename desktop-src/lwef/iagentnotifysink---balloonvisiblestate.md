---
title: Iagentnotifysink balloonvisiblestate
description: Iagentnotifysink balloonvisiblestate
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340221"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a>Iagentnotifysink:: balloonvisiblestate

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

Benachrichtigt eine Client Anwendung, wenn sich der Sichtbarkeits Zustand der Wort Sprechblase des Zeichens ändert.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, dessen Sichtbarkeits Zustand der Word-Sprechblase geändert wurde.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Sichtbarkeits Kennzeichen. Dieser boolesche Wert ist **true** , wenn die Wort Sprechblase des Zeichens sichtbar wird. und **false** , wenn es ausgeblendet wird.

</dd> </dl>

Dieses Ereignis wird an alle Clients des Zeichens gesendet.

 

 




