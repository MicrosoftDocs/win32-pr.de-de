---
description: Wird von der Pipeline an Encoder-MFTs seriell mit Medienbeispielen über DIE ÜBERTRANSFORM::P rocessEvent gesendet.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: MEEncodingParameters-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2230640adf1f92111569a39558f2959271a23ea2b5dbe5d0d915b6a2b989d371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723830"
---
# <a name="meencodingparameters-event"></a>MEEncodingParameters-Ereignis

Wird von der Pipeline an Encoder-MFTs seriell mit Medienbeispielen über [**DIETRANSFORM::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                         | Beschreibung                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | Enthält die neuen ICodecAPI-basierten Einstellungen, die der Encoder auf nachfolgende eingehende Stichproben anwenden soll.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Bei der Ereignisnutzlast handelt es sich um einen Attributspeicher (POINTERAttributes-Zeiger), der die neuen ICodecAPI-basierten /-Einstellungen enthält, die der Encoder auf nachfolgende eingehende Stichproben anwenden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




