---
description: Die \_ LINEAGENTSESSIONSTATE-Konstanten beschreiben verschiedene Agent-Sitzungszustände.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: LINEAGENTSESSIONSTATE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702c9820fb6c2157a386241b13ea0593c4156195bc74bcfa7655c76db171083d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682200"
---
# <a name="lineagentsessionstate_-constants"></a>LINEAGENTSESSIONSTATE-Konstanten \_

Die **\_ LINEAGENTSESSIONSTATE-Konstanten beschreiben** verschiedene Agent-Sitzungszustände.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**
</dt> <dd> <dl> <dt>



Der Agent ist damit beschäftigt, einen Aufruf zu behandeln.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**
</dt> <dd> <dl> <dt>



Der Agent ist damit beschäftigt, die Zusammenfassung des Aufrufs zu behandeln.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ BEENDET**
</dt> <dd> <dl> <dt>



Die Agentsitzung wurde beendet.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOTREADY**
</dt> <dd> <dl> <dt>



Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Bedienen eines Aufrufs (z. B. bei einer Unterbrechung) beschäftigt. Es sollten keine zusätzlichen Aufrufe an den Agent geroutet werden.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ READY**
</dt> <dd> <dl> <dt>



Der Agent ist bereit, Aufrufe zu akzeptieren.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ VERÖFFENTLICHT**
</dt> <dd> <dl> <dt>



Die Agentsitzung wurde freigegeben.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




