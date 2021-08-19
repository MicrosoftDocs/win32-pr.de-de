---
description: Präsentationszeit für ein Beispiel, das während der Bereinigung gerendert wurde.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: MF_EVENT_SCRUBSAMPLE_TIME Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57045fcf5fd4faf20d2207778b91aa8ff0fd959dd42571882a21b5a1dceacba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104816"
---
# <a name="mf_event_scrubsample_time-attribute"></a>MF \_ EVENT \_ SCRUBSAMPLE \_ TIME-Attribut

Präsentationszeit für ein Beispiel, das während der Bereinigung gerendert wurde.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut wird mit dem [MEStreamSinkScrubSampleComplete-Ereignis](mestreamsinkscrubsamplecomplete.md) verwendet.

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

 

 




