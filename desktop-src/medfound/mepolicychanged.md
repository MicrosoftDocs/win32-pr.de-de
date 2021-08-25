---
description: Wird von einer Pipelinekomponente ausgelöst, wenn sich die Ausgaberichtlinie für den Stream ändert. Dieses Ereignis gilt nur für geschützten Inhalt.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: MEPolicyChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957410"
---
# <a name="mepolicychanged-event"></a>MEPolicyChanged-Ereignis

Wird von einer Pipelinekomponente ausgelöst, wenn sich die Ausgaberichtlinie für den Stream ändert. Dieses Ereignis gilt nur für geschützten Inhalt.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE                | BESCHREIBUNG                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Zeiger auf die [**BENUTZEROBERFLÄCHEOutputPolicy-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) der neuen Richtlinie für den Stream.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis muss von allen vertrauenswürdigen Ausgaben behandelt werden. Media Foundation -Transformationen (MFTs) empfangen dieses Ereignis über die [**METHODE VORRTRANSFORM::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Mediensenken empfangen dieses Ereignis über die [**METHODE :P STREAMSink::P Marker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

Die vertrauenswürdige Ausgabe muss die neue Richtlinie anwenden oder den Fehlercode MF \_ E \_ POLICY \_ UNSUPPORTED zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




