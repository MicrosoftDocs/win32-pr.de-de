---
title: Iagentcharacter-Wartezeit
description: Iagentcharacter-Wartezeit
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310747"
---
# <a name="iagentcharacterwait"></a>Iagentcharacter:: Wait

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Enthält die Animations Warteschlange des Zeichens bei der angegebenen Animation (Anforderung), bis eine andere Anforderung für ein anderes Zeichen abgeschlossen ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*
</dt> <dd>

Die ID der Anforderung, auf die gewartet werden soll.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die **warte** Anforderungs-ID empfängt.

</dd> </dl>

Verwenden Sie diese Methode nur, wenn Sie mehrere (gleichzeitige) Zeichen unterstützen und ihre Interaktion Sequenzieren möchten. (Bei einem einzelnen Zeichen wird jede Animations Anforderung sequenziell wiedergegeben, nachdem die vorherige Anforderung abgeschlossen wurde.) Wenn Sie zwei Zeichen haben und möchten, dass die Animations Anforderung eines Zeichens wartet, bis die Animation des anderen Zeichens abgeschlossen ist, legen Sie die **Wait** -Methode auf die Animations Anforderungs-ID des anderen Zeichens fest.

 

 




