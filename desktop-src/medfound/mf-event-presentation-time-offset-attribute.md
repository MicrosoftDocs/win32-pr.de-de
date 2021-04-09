---
description: Offset zwischen der Präsentationszeit und den Medienquellen-Zeitstempeln.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: MF_EVENT_PRESENTATION_TIME_OFFSET-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862959"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>\_ \_ \_ Zeit \_ Offset Attribut der MF-Ereignis Präsentation

Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Der Offset wird wie folgt berechnet: Offset = Präsentationszeit-Quell Zeit. Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [Mesessionnotifypresentationtime](mesessionnotifypresentationtime.md)
-   [Mesessionstarted](mesessionstarted.md)

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

 

 




