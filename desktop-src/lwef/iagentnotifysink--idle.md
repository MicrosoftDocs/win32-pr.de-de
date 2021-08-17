---
title: IAgentNotifySink Idle
description: IAgentNotifySink Idle
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105172"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink::Idle

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Benachrichtigt eine Clientanwendung, wenn sich der **Idling-Zustand** eines Zeichens geändert hat.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner der gestarteten Anforderung.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

Startflag. Dieser boolesche Wert ist **True,** wenn das Zeichen mit dem Leerlauf beginnt, und **False,** wenn es nicht mehr leer ist.

</dd> </dl>

Mit diesem Ereignis können Sie nachverfolgen, wann der Microsoft-Agent-Server die Leerlaufverarbeitung für ein Zeichen startet oder beendet.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




