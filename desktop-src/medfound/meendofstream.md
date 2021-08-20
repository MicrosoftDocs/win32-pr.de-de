---
description: Wird von einem Medienstream ausgelöst, wenn der Stream endet.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: MEEndOfStream-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23a2db351d31558a617b72a8640d121b71c866021063d4791d19797108f34819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877773"
---
# <a name="meendofstream-event"></a>MEEndOfStream-Ereignis

Wird von einem Medienstream ausgelöst, wenn der Stream endet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Wenn die [Mediensitzung](media-session.md) das MEEndOfStream-Ereignis empfängt, ruft sie [**DIE DENSTREAMSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) für die entsprechende Mediensenke mit dem **MFSTREAMSINK \_ MARKER \_ ENDOFSEGMENT-Markertyp** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




