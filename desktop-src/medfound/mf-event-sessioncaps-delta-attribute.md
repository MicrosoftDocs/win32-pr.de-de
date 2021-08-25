---
description: Enthält Flags, die angeben, welche Funktionen sich in der Mediensitzung basierend auf der aktuellen Präsentation geändert haben.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714841"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>MF \_ EVENT \_ SESSIONCAPS \_ DELTA-Attribut

Enthält Flags, die angeben, welche Funktionen sich in der Mediensitzung basierend auf der aktuellen Präsentation geändert haben.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut enthält eine Bitmaske, die angibt, welche Funktionenflags geändert wurden. Eine Liste der möglichen Flags finden Sie unter 1000000000000000000000000000000000000000000000000 [](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) Bits werden in der Bitmaske aus einem der folgenden Gründe auf 1 festgelegt:

-   Das entsprechende Funktionenbit wurde von 0 in 1 geändert.
-   Das entsprechende Funktionenbit wurde von 1 in 0 geändert.
-   Das entsprechende Funktionsbit bleibt 1, aber die Details der Funktion haben sich geändert. Beispielsweise hat sich die maximale Wiedergaberate geändert.

Dieses Attribut wird mit dem [MESessionCapabilitiesChanged-Ereignis](mesessioncapabilitieschanged.md) verwendet.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




