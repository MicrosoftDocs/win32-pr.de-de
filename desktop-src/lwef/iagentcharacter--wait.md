---
title: IAgentCharacter Wait
description: IAgentCharacter Wait
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014220"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter::Wait

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Enthält die Animationswarteschlange des Zeichens an der angegebenen Animation (Anforderung), bis eine andere Anforderung für ein anderes Zeichen abgeschlossen ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Die ID der Anforderung, auf die gewartet werden soll.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die  die Wait-Anforderungs-ID empfängt.

</dd> </dl>

Verwenden Sie diese Methode nur, wenn Sie mehrere (gleichzeitige) Zeichen unterstützen und deren Interaktion sequenzieren möchten. (Für ein einzelnes Zeichen wird jede Animationsanforderung sequenziell wiedergegeben , nachdem die vorherige Anforderung abgeschlossen wurde.) Wenn Sie zwei Zeichen haben und die Animationsanforderung eines Zeichens warten soll, bis die Animation des anderen Zeichens abgeschlossen ist, legen Sie die **Wait-Methode** auf die Animationsanforderungs-ID des anderen Zeichens fest.

 

 




