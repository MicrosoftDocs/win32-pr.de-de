---
description: Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, um ein neues Eingabe Beispiel anzufordern.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Metransformneedinput-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129805"
---
# <a name="metransformneedinput-event"></a>Metransformneedinput-Ereignis

Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, um ein neues Eingabe Beispiel anzufordern.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG               |
|----------------------|---------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                        | BESCHREIBUNG                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [\_ \_ MFT- \_ Eingabedaten \_ Strom- \_ ID des MF-Ereignisses](mf-event-mft-input-stream-id.md)<br/> | Der Bezeichner des Streams, der Eingabedaten benötigt.<br/>*Benötigten*<br/> |



## <a name="remarks"></a>Bemerkungen

Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle. Dieses Ereignis wird von synchronen MFTs niemals gesendet.

Wenn der Client der MFT dieses Ereignis empfängt, sollte er [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufrufen, um das nächste Beispiel bereitzustellen. Das [MF- \_ Ereignis \_ MFT-Eingabedaten Strom- \_ \_ \_ ID](mf-event-mft-input-stream-id.md) -Attribut des Ereignis Objekts gibt an, welcher Eingabedaten Strom Daten erfordert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




