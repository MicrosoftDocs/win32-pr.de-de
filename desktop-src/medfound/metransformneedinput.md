---
description: Wird von einer asynchronen Media Foundation Transformierung (MFT) gesendet, um ein neues Eingabebeispiel an fordern.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: METransformNeedInput-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013500"
---
# <a name="metransformneedinput-event"></a>METransformNeedInput-Ereignis

Wird von einer asynchronen Media Foundation Transformierung (MFT) gesendet, um ein neues Eingabebeispiel an fordern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                        | Beschreibung                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ \_ \_ MF-EREIGNIS-MFT-EINGABESTREAM-ID \_ \_](mf-event-mft-input-stream-id.md)<br/> | Der Bezeichner des Streams, der Eingabedaten benötigt.<br/>*(Erforderlich)*<br/> |



## <a name="remarks"></a>Hinweise

Asynchrone MFTs senden dieses Ereignis über die [**BEFIMediaEventGenerator-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Synchrone MFTs senden dieses Ereignis nie.

Wenn der Client des MFT dieses Ereignis empfängt, sollte [**er DIETRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufrufen, um das nächste Beispiel zu liefern. Das [MF \_ EVENT \_ MFT INPUT STREAM \_ \_ \_ ID-Attribut](mf-event-mft-input-stream-id.md) des Ereignisobjekts gibt an, welcher Eingabestream Daten erfordert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




