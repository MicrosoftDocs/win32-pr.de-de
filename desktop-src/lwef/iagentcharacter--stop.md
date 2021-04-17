---
title: Iagentcharacter-Vorgang wird beendet
description: Iagentcharacter-Vorgang wird beendet
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388563"
---
# <a name="iagentcharacterstop"></a>Iagentcharacter:: Beendigung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Beendet die angegebene Animation (Anforderung) und entfernt Sie aus der Animations Warteschlange des Zeichens.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwreqid*
</dt> <dd>

Die ID der Anforderung, die angehalten werden soll.

</dd> </dl>

**Stop** kann auch verwendet werden, um alle [**Vorbereitungs**](iagentcharacter--prepare.md) Aufrufe in der Warteschlange anzuhalten.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter::P repare**](iagentcharacter--prepare.md), [ **iagentcharacter:: stopAll**](iagentcharacter--stopall.md)


 

 




