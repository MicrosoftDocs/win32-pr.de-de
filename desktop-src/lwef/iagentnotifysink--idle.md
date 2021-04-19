---
title: Iagentnotifysink im Leerlauf
description: Iagentnotifysink im Leerlauf
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339437"
---
# <a name="iagentnotifysinkidle"></a>Iagentnotifysink:: Leerlauf

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Benachrichtigt eine Client Anwendung, wenn sich der **Leerlauf** Zustand eines Zeichens geändert hat.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner der Anforderung, die gestartet wurde.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

Startflag. Dieser boolesche Wert ist **true** , wenn das Zeichen mit der Leerlaufzeit beginnt, und **false** , wenn es nicht mehr reagiert.

</dd> </dl>

Mithilfe dieses Ereignisses können Sie nachverfolgen, wann der Microsoft-Agent-Server die Leerlauf Verarbeitung für ein Zeichen startet oder beendet.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: getidleon**](iagentcharacter--getidleon.md), [ **iagentcharacter:: abtidleon**](iagentcharacter--setidleon.md)


 

 




