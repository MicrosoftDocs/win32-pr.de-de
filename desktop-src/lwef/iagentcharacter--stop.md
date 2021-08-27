---
title: IAgentCharacter Stop
description: IAgentCharacter Stop
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114780"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter::Stop

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Beendet die angegebene Animation (Anforderung) und entfernt sie aus der Animationswarteschlange des Zeichens.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Die ID der zu beendenden Anforderung.

</dd> </dl>

**Stop** kann auch verwendet werden, um alle Aufrufe der Prepare-Vorbereitung in der [**Warteschlange anzuhalten.**](iagentcharacter--prepare.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter::StopAll**](iagentcharacter--stopall.md)


 

 




