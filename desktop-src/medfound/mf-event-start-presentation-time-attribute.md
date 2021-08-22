---
description: Die Startzeit für die Präsentation in Einheiten von 100 Nanosekunden, gemessen an der Präsentationsuhr.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: MF_EVENT_START_PRESENTATION_TIME-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd623677de67d2101f4b1cbb3e17ce429f37f0788d99f802be0889a35dd3471e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104826"
---
# <a name="mf_event_start_presentation_time-attribute"></a>MF \_ EVENT START PRESENTATION \_ \_ \_ TIME-Attribut

Die Startzeit für die Präsentation in Einheiten von 100 Nanosekunden, gemessen an der Präsentationsuhr.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit dem [MESessionNotifyPresentationTime-Ereignis](mesessionnotifypresentationtime.md) verwendet.

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl es als **UINT64** gespeichert ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




