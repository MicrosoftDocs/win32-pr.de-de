---
description: Signalisiert den Fortschritt eines Content Enabler-Objekts. Objekte, die die SCHNITTSTELLE "CONTENTContentEnabler" verfügbar machen, können dieses Ereignis auslösen, um die Anwendung über den Fortschritt der Content Enabler-Aktionen zu benachrichtigen.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: MEEnablerProgress-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9772a076e1d9de0cff2336b4c6d6b9b068f11e4fc572b44f0f914a8353f651bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013760"
---
# <a name="meenablerprogress-event"></a>MEEnablerProgress-Ereignis

Signalisiert den Fortschritt eines Content Enabler-Objekts. Objekte, die die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) verfügbar machen, können dieses Ereignis auslösen, um die Anwendung über den Fortschritt der Aktionen des Content Enablers zu benachrichtigen.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE               | Beschreibung                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | Breitzeichenzeichenfolge, die den Fortschritt beschreibt.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Um dieses Ereignis zu empfangen, fragen Sie die [**SCHNITTSTELLE "CONTENTContentEnabler"**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) nach der [**SCHNITTSTELLE "ARRANGEMediaEventGenerator"**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) ab. Rufen Sie dann [**DENMEDIAEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)auf, wie im Thema [Medienereignisgeneratoren](media-event-generators.md)beschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CONTENTContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[Medienereignisgeneratoren](media-event-generators.md)
</dt> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




