---
description: Gibt an, ob die Sequencerquelle eine Topologie abgebrochen hat.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef612c8a1081ecc26eaa9dc593a5906ff965d0387ab02490eedd68f7fbf5e813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060657"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>\_ \_ CANCELED-Attribut der \_ \_ MF-EREIGNISQUELLENTOPOLOGIE

Gibt an, ob [die Sequencerquelle](sequencer-source.md) eine Topologie abgebrochen hat.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Wenn dieses Attribut vorhanden ist und ungleich 0 (null) ist, bedeutet dies, dass das Präsentationssegment beendet wurde, da die Sequencerquelle die Topologie abgebrochen hat. Andernfalls wurde das Präsentationssegment normal beendet.

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

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Sequencer-Quellereignisse](sequencer-source-events.md)
</dt> </dl>

 

 




