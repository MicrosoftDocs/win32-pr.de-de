---
description: Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a31b1970c2c9d86384c12c50777a8cee55e3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364077"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>MF- \_ Sitzung \_ ca. \_ Ereignis \_ vorkommen \_ Zeit Attribut

Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Einige Ereignisse aus der Medien Sitzung verfügen über dieses Attribut. Der-Wert gibt die ungefähre Präsentationszeit an, zu der das-Ereignis ausgelöst wurde.

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

 

 




