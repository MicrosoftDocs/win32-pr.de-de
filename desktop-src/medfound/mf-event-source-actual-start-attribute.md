---
description: Enthält die Startzeit, zu der eine Medienquelle von ihrer aktuellen Position neu gestartet wird.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ce39e8a9f90ad0cd7f0cbd590b32719ab10dbd8e498c396e86772ce333e94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104836"
---
# <a name="mf_event_source_actual_start-attribute"></a>MF \_ EVENT SOURCE ACTUAL \_ \_ \_ START-Attribut

Enthält die Startzeit, zu der eine Medienquelle von ihrer aktuellen Position neu gestartet wird.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit dem [MESourceStarted-Ereignis](mesourcestarted.md) verwendet. Das -Attribut ist relevant, wenn die Ereignisdaten leer sind (**VT \_ EMPTY**), was angibt, dass die Medienquelle von der aktuellen Wiedergabeposition gestartet wurde. In diesem Fall gibt das **MF \_ EVENT SOURCE \_ ACTUAL \_ \_ START-Attribut** die tatsächliche Startzeit an. Wenn die Ereignisdaten **VT \_ EMPTY** sind und dieses Attribut nicht festgelegt ist, wird davon ausgegangen, dass die Startzeit null ist.

Wenn die [MESourceStarted-Ereignisdaten](mesourcestarted.md) die Startzeit **(VT \_ I8)** enthalten, sollte dieses Attribut nicht festgelegt werden.

Dieses Attribut ist ein signierter Wert, obwohl es als **UINT64 gespeichert wird.**

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEs::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




