---
description: Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866188"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_ \_ \_ Zeitpunkt der Präsentation des MF-Ereignisses \_ \_ beim \_ Ausgabe Attribut

Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Wenn alle Pipeline Objekte in der vorherigen Topologie Daten gepuffert haben, ist dieser Wert etwas niedriger als der Wert im [**\_ \_ \_ Zeit \_ Offset Attribut der MF-Ereignis Präsentation**](mf-event-presentation-time-offset-attribute.md) , da die senken die gepufferten Daten renderten müssen.

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.

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

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




