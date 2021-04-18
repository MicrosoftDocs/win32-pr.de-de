---
description: Die lineagentsessionstate- \_ Konstanten beschreiben verschiedene agentsitzungszustände.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: LINEAGENTSESSIONSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364948"
---
# <a name="lineagentsessionstate_-constants"></a>Lineagentsessionstate- \_ Konstanten

Die **lineagentsessionstate- \_ Konstanten** beschreiben verschiedene agentsitzungszustände.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**lineagentsessionstate \_ busyoncallcenter**
</dt> <dd> <dl> <dt>



Der Agent ist mit der Verarbeitung eines Aufrufes ausgelastet.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**lineagentsessionstate \_ busywrapup**
</dt> <dd> <dl> <dt>



Der Agent ist ausgelastet, um die Zusammenfassung des Aufrufes aufzurufen.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**lineagentsessionstate wurde \_ beendet.**
</dt> <dd> <dl> <dt>



Die Agentsitzung wurde beendet.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**lineagentsessionstate \_ notready**
</dt> <dd> <dl> <dt>



Der Agent ist angemeldet, aber mit einer anderen Aufgabe als dem Ausführen eines Aufrufens (z. b. bei einer Unterbrechung) beschäftigt. Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**lineagentsessionstate ist \_ bereit**
</dt> <dd> <dl> <dt>



Der Agent ist zum Akzeptieren von Aufrufen bereit.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**lineagentsessionstate \_ veröffentlicht**
</dt> <dd> <dl> <dt>



Die Agentsitzung wurde freigegeben.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




