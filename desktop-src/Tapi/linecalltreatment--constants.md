---
description: Die LINECALLTREATMENT-Konstanten \_ listen Aufrufe auf, die nicht beantwortet oder zurückgehalten werden. Mit Ausnahme der grundlegenden Parametervalidierung ist die Anrufbehandlung eine direkte Übergabe durch TAPI an den Dienstanbieter.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: LINECALLTREATMENT_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88c627a89fdf5ab0592c862f09753e0b913eb4b7197a04d4db8cd06478ef10b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863838"
---
# <a name="linecalltreatment_-constants"></a>LINECALLTREATMENT-Konstanten \_

Die **\_ LINECALLTREATMENT-Konstanten** listen Aufrufe auf, die nicht beantwortet oder zurückgehalten werden. Mit Ausnahme der grundlegenden Parametervalidierung ist die Anrufbehandlung eine direkte Übergabe durch TAPI an den Dienstanbieter.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ AUSGELASTET**
</dt> <dd> <dl> <dt>



Wenn der Anruf nicht aktiv mit einem Gerät (Angebot oder Onhold) verbunden ist, wird das Signal "Ausgelastet" von der Partei gehört.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT \_ MUSIC**
</dt> <dd> <dl> <dt>



Wenn der Anruf nicht aktiv mit einem Gerät (Angebot oder Onhold) verbunden ist, hören die Party Musik.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT \_ RINGBACK**
</dt> <dd> <dl> <dt>



Wenn der Anruf nicht aktiv mit einem Gerät verbunden ist (Angebot oder Onhold), wird der Ringbackton von der Partei gehört.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT \_ SILENCE**
</dt> <dd> <dl> <dt>



Wenn der Anruf nicht aktiv mit einem Gerät verbunden ist (Angebot oder Onhold), hören die Parteien Stille.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Der Wert 0x00000000 reserviert ist, um anzugeben, dass der Dienstanbieter anruft. Werte im Bereich 0x00000005 bis 0x000000FF sind für zukünftige Definitionen reserviert. Werte im Bereich 0x00000100 bis 0xFFFFFFFF sind für die Zuweisung durch Dienstanbieter reserviert und können die Identifizierung bestimmter Auswahlmöglichkeiten oder aufgezeichneter Ankündigungen umfassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




