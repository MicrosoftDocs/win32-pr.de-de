---
description: Gibt an, ob die Sequencer-Quelle eine Topologie abgebrochen hat.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366249"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>Attribut der MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen.

Gibt an, ob die [Sequencer-Quelle](sequencer-source.md) eine Topologie abgebrochen hat.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [Meendof presentationsegment](meendofpresentationsegment.md)
-   [Meendof Presentation](meendofpresentation.md)

Wenn dieses Attribut vorhanden und ungleich NULL ist, bedeutet dies, dass das Präsentations Segment beendet wurde, weil die Sequencer-Quelle die Topologie abgebrochen hat. Andernfalls wurde das Präsentations Segment normal beendet.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Sequencer-Quell Ereignisse](sequencer-source-events.md)
</dt> </dl>

 

 




