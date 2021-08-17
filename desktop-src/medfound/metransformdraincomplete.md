---
description: Wird von einer asynchronen Media Foundation Transformation (MFT) gesendet, wenn ein Entleerungsvorgang abgeschlossen ist.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: METransformDrainComplete-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974029"
---
# <a name="metransformdraincomplete-event"></a>METransformDrainComplete-Ereignis

Wird von einer asynchronen Media Foundation Transformation (MFT) gesendet, wenn ein Entleerungsvorgang abgeschlossen ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                        | Beschreibung                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [\_ \_ \_ \_ MFT-EINGABESTREAM-ID des MF-EREIGNISSES \_](mf-event-mft-input-stream-id.md)<br/> | Der Bezeichner des Datenstroms, der entladen wurde.<br/>*(Erforderlich)*<br/> |



## <a name="remarks"></a>Hinweise

Asynchrone MFTs senden dieses Ereignis über die [**INTERFACESMediaEventGenerator-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Synchrone MFTs senden dieses Ereignis nie.

Um einen MFT zu entladen, rufen Sie [**ÜBERTRANSFORM::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **Meldung MFT \_ MESSAGE COMMAND \_ \_ DRAIN** auf. Geben Sie den Eingabestream an, der im *ulParam-Parameter* entladen werden soll. Wenn der Entleerungsvorgang abgeschlossen ist, sendet ein asynchroner MFT das METransformDrainComplete-Ereignis. Das [MF \_ EVENT \_ MFT INPUT STREAM \_ \_ \_ ID-Attribut](mf-event-mft-input-stream-id.md) des Ereignisses enthält den Streambezeichner, der im *ulParam-Parameter* angegeben ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




