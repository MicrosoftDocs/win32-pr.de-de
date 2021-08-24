---
description: Die Präsentationszeit, zu der die Mediensenken das erste Beispiel der neuen Topologie rendern.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd5949a73244eec26fb0390805c11f630291a470b2016b5a3575311261b72a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723180"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>MF \_ EVENT START PRESENTATION TIME AT \_ \_ \_ \_ \_ OUTPUT-Attribut

Die Präsentationszeit, zu der die Mediensenken das erste Beispiel der neuen Topologie rendern.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Wenn Pipelineobjekte in den zuvor gepufferten Topologiedaten enthalten sind, ist dieser Wert etwas kleiner als der Wert im [**MF \_ EVENT PRESENTATION \_ TIME \_ \_ OFFSET-Attribut,**](mf-event-presentation-time-offset-attribute.md) da die Senken die gepufferten Daten rendern müssen.

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

 

 




