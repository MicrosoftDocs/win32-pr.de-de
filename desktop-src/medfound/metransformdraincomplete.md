---
description: Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn ein Ausgleichs Vorgang beendet ist.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Metransformdraunvollereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348748"
---
# <a name="metransformdraincomplete-event"></a>Metransformdraunvollständiges Ereignis

Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn ein Ausgleichs Vorgang beendet ist.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG               |
|----------------------|---------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                        | BESCHREIBUNG                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [\_ \_ MFT- \_ Eingabedaten \_ Strom- \_ ID des MF-Ereignisses](mf-event-mft-input-stream-id.md)<br/> | Der Bezeichner des Datenstroms, der entladen wurde.<br/>*Benötigten*<br/> |



## <a name="remarks"></a>Bemerkungen

Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle. Dieses Ereignis wird von synchronen MFTs niemals gesendet.

Um einen MFT zu entleeren, wenden Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **MFT- \_ Nachrichten \_ Befehls \_** Ausgleichs Meldung an. Geben Sie den Eingabedaten Strom an, der im *ulparam* -Parameter geleert werden soll. Wenn der Ausgleichs Vorgang abgeschlossen ist, sendet eine asynchrone MFT das metransformdraunvoll-Ereignis. Das [MF- \_ Ereignis \_ MFT-Eingabedaten Strom- \_ \_ \_ ID](mf-event-mft-input-stream-id.md) -Attribut des Ereignisses enthält den im *ulparam* -Parameter angegebenen Datenstrom Bezeichner.

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

 

 




