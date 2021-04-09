---
description: Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: MF_EVENT_START_PRESENTATION_TIME-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf6142ce12a7bf921fd26373ea5d10ab384560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050611"
---
# <a name="mf_event_start_presentation_time-attribute"></a>Zeit Attribut der MF- \_ Ereignis \_ Start \_ Präsentation \_

Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird mit dem [mesessionnotifypresentationtime](mesessionnotifypresentationtime.md) -Ereignis verwendet.

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

 

 




