---
description: Die LINEAGENTSTATEEX-Konstanten \_ beschreiben den Zustand eines Agents für eine Adresse.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140093"
---
# <a name="lineagentstateex_-constants"></a>\_LINEAGENTSTATEEX-Konstanten

Die **LINEAGENTSTATEEX-Konstanten \_** beschreiben den Zustand eines Agents für eine Adresse.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



Der Agent ist mit der Verarbeitung eines Aufrufs ausgelastet, der von einer ACD-Warteschlange weitergeleitet wird.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



Der Agent ist mit der Verarbeitung eines eingehenden Aufrufs beschäftigt, der nicht aus einer ACD-Warteschlange, in der der Agent angemeldet ist, an den Agent übertragen wurde.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



Der Agent ist mit der Verarbeitung eines ausgehenden Anrufs beschäftigt, z. B. eines Anrufs, der von einer Warteschlange für Vorhersagewähle weitergeleitet wird.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**
</dt> <dd> <dl> <dt>



Der Agent ist angemeldet, wird aber mit einer anderen Aufgabe als der Bereitstellung eines Anrufs (z. B. bei einer Unterbrechung) belegt. Es sollten keine weiteren Aufrufe an den Agent weitergeleitet werden.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ READY**
</dt> <dd> <dl> <dt>



Der Agent ist bereit, Aufrufe zu akzeptieren.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ VERÖFFENTLICHT**
</dt> <dd> <dl> <dt>



Der Agent wurde freigegeben, wahrscheinlich weil er abgemeldet wurde.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Der Agent-Status ist derzeit unbekannt, kann aber später bekannt werden. Dies kann ein Übergangszustand sein, wenn eine Zeile oder Adresse zum ersten Mal geöffnet wird.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




