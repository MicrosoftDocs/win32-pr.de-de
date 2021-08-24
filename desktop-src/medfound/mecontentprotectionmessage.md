---
description: Wird von einer Pipelinekomponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabeschutzschemas ändert. Dieses Ereignis gilt nur für geschützten Inhalt.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: MEContentProtectionMessage-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0316767025fe4446909146b92cfcea8abcc3e0511990c19485a50c94dbc3fa59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013830"
---
# <a name="mecontentprotectionmessage-event"></a>MEContentProtectionMessage-Ereignis

Wird von einer Pipelinekomponente ausgelöst, wenn sich die Konfiguration für eines der Ausgabeschutzschemas ändert. Dieses Ereignis gilt nur für geschützten Inhalt.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis muss von allen vertrauenswürdigen Ausgaben behandelt werden. Media Foundation -Transformationen (MFTs) empfangen dieses Ereignis über die [**METHODE ROCTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Mediensenken empfangen dieses Ereignis über die [**METHODE VORZEICHENStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

Die vertrauenswürdige Ausgabe muss die Richtlinienänderungen anwenden oder den Fehlercode MF \_ E \_ POLICY \_ UNSUPPORTED zurückgeben.

Die Ereignisdaten und Attribute hängen vom verwendeten Inhaltsschutzsystem ab.

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

 

 




