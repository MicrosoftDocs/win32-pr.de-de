---
description: Wird von einer asynchronen Media Foundation-Transformation (MFT) als Reaktion auf eine MFT \_ MESSAGE \_ COMMAND \_ MARKER-Nachricht gesendet.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: METransformMarker-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7029119b30314e56531c0afb29accadb67e1efb343a906c2558af2157c0b1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827040"
---
# <a name="metransformmarker-event"></a>METransformMarker-Ereignis

Wird von einer asynchronen Media Foundation-Transformation (MFT) als Antwort auf eine **MFT \_ MESSAGE COMMAND \_ \_ MARKER-Nachricht** gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                      | Beschreibung                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MF \_ EVENT \_ MFT \_ CONTEXT](mf-event-mft-context.md)<br/> | Der Wert des *ulParam-Parameters* aus der **MFT \_ MESSAGE COMMAND \_ \_ MARKER-Nachricht.**<br/>*(Erforderlich)*<br/> |



## <a name="remarks"></a>Hinweise

Asynchrone MFTs senden dieses Ereignis über die [**INTERFACESMediaEventGenerator-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Synchrone MFTs senden dieses Ereignis nie.

Der Client eines asynchronen MFT kann einen Marker im Datenstrom platzieren, indem [**ERFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **MFT \_ MESSAGE COMMAND \_ \_ MARKER-Nachricht** aufruft. Der *ulParam-Parameter* enthält anwendungsdefinierte Daten.

Wenn der MFT die Verarbeitung aller Eingabedaten abgeschlossen hat, die zum Zeitpunkt des [**ProcessMessage-Aufrufs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) verfügbar waren, stellt der MFT ein METransformMarker-Ereignis in die Warteschlange. Das [MF \_ EVENT \_ MFT \_ CONTEXT-Attribut](mf-event-mft-context.md) des Ereignisses enthält den Wert des *ulParam-Parameters.* Weitere Informationen finden Sie unter [Asynchrone MFTs.](asynchronous-mfts.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




