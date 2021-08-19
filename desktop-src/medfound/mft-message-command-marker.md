---
description: Markiert einen Punkt im Stream. Diese Meldung gilt nur für asynchrone MFTs.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc55a96ae9680b37d83ec776c66848ed04f4a30b62d1d0378035c88823d2c19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872170"
---
# <a name="mft_message_command_marker"></a>MFT \_ MESSAGE \_ COMMAND \_ MARKER

Markiert einen Punkt im Stream. Diese Meldung gilt nur für [asynchrone MFTs.](asynchronous-mfts.md)

## <a name="message-parameter"></a>Message-Parameter

Ein beliebiger Wert. Der MFT gibt den Wert im [METransformMarker-Ereignis](metransformmarker.md) an den Client zurück.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen [**Sie DIETRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

MFT antwortet wie folgt auf diese Meldung:

1.  MFT generiert so viele Ausgabebeispiele wie möglich aus den vorhandenen Eingabedaten und sendet für jedes Ausgabebeispiel ein [METransformHaveOutput-Ereignis.](metransformhaveoutput.md)
2.  Nachdem die ganze Ausgabe generiert wurde, sendet MFT ein [METransformMarker-Ereignis.](metransformmarker.md) Dieses Ereignis muss nach allen [METransformHaveOutput-Ereignissen gesendet](metransformhaveoutput.md) werden.

Der Client ist nicht zum Senden dieser Nachricht erforderlich und sollte diese Nachricht nur an asynchrone MFTs senden. Ein synchrones MFT sendet kein [METransformMarker-Ereignis](metransformmarker.md) als Antwort auf diese Nachricht.

### <a name="implementation"></a>Implementierung

Asynchrone MFTs müssen wie beschrieben auf diese Meldung reagieren. Synchrone MFTs sollten diese Meldung ignorieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




