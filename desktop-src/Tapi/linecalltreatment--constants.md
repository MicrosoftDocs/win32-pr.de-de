---
description: Die linecalltreatment- \_ Konstanten Listen Behandlungen für Aufrufe auf, die nicht beantwortet werden oder angehalten sind. Mit Ausnahme der grundlegenden Parameter Validierung ist die aufrufsbehandlung ein geradliniges Pass-Through von TAPI zum Dienstanbieter.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: LINECALLTREATMENT_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373980"
---
# <a name="linecalltreatment_-constants"></a>Linecalltreatment- \_ Konstanten

Die **linecalltreatment \_** -Konstanten Listen Behandlungen für Aufrufe auf, die nicht beantwortet werden oder angehalten sind. Mit Ausnahme der grundlegenden Parameter Validierung ist die aufrufsbehandlung ein geradliniges Pass-Through von TAPI zum Dienstanbieter.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**linecalltreatment \_ ausgelastet**
</dt> <dd> <dl> <dt>



Wenn der-Rückruf nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei das ausgelastete Signal.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**linecalltreatment- \_ Musik**
</dt> <dd> <dl> <dt>



Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei Musik.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**linecalltreatment- \_ Rollback**
</dt> <dd> <dl> <dt>



Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei den ringbackton.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**Ruhe Behandlung in linecalltreatment \_**
</dt> <dd> <dl> <dt>



Wenn der-Befehl nicht aktiv mit einem Gerät (Angebot oder OnHold) verbunden ist, hört die Partei Ruhe.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Wert 0x00000000 ist reserviert, um anzugeben, dass der Dienstanbieter keine aufrufsbehandlungen unterstützt. Werte im Bereich 0x00000005 bei der bis 0x000000ff sind für zukünftige Definitionen reserviert. Werte im Bereich 0x00000100 bis 0xffffffff sind für die Zuweisung durch Dienstanbieter reserviert und können die Identifizierung bestimmter musikalischer oder aufgezeichneter Ankündigungen einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




