---
description: Wird durch eine asynchrone Media Foundation Transformation (MFT) als Antwort auf eine MFT- \_ Nachrichten \_ Befehls \_ markernachricht gesendet.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Metransformmarker-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354602"
---
# <a name="metransformmarker-event"></a>Metransformmarker-Ereignis

Wird durch eine asynchrone Media Foundation Transformation (MFT) als Antwort auf eine **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG               |
|----------------------|---------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                      | BESCHREIBUNG                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ MFT- \_ Kontext für MF-Ereignis](mf-event-mft-context.md)<br/> | Der Wert des *ulparam* -Parameters aus der **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** .<br/>*Benötigten*<br/> |



## <a name="remarks"></a>Bemerkungen

Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle. Dieses Ereignis wird von synchronen MFTs niemals gesendet.

Der Client einer asynchronen MFT kann einen Marker im Stream platzieren, indem er [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** aufruft. Der *ulparam* -Parameter enthält Anwendungs definierte Daten.

Wenn die MFT die Verarbeitung aller Eingabedaten abgeschlossen hat, die zum Zeitpunkt des [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) -Aufrufes aufgerufen wurden, fügt die MFT ein metransformmarker-Ereignis in die Warteschlange ein. Das [ \_ \_ MFT- \_ Kontext](mf-event-mft-context.md) Attribut des MF-Ereignisses des Ereignisses enthält den Wert des *ulparam* -Parameters. Weitere Informationen finden Sie unter [asynchrone MFTs](asynchronous-mfts.md).

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

 

 




