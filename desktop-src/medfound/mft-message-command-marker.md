---
description: Markiert einen Punkt im Stream. Diese Meldung gilt nur für asynchrone MFTs.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368231"
---
# <a name="mft_message_command_marker"></a>MFT- \_ Nachrichten \_ Befehls \_ Marker

Markiert einen Punkt im Stream. Diese Meldung gilt nur für [asynchrone MFTs](asynchronous-mfts.md).

## <a name="message-parameter"></a>Message-Parameter

Ein beliebiger Wert. Der MFT gibt den Wert im [metransformmarker](metransformmarker.md) -Ereignis an den Client zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Die MFT antwortet auf diese messageas:

1.  Der MFT generiert so viele Ausgabe Beispiele wie aus den vorhandenen Eingabedaten und sendet ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis für jedes Ausgabe Beispiel.
2.  Nachdem die gesamte Ausgabe generiert wurde, sendet der MFT ein [metransformmarker](metransformmarker.md) -Ereignis. Dieses Ereignis muss nach allen [metransformhaveoutput](metransformhaveoutput.md) -Ereignissen gesendet werden.

Der Client muss diese Nachricht nicht senden und sollte diese Nachricht nur an asynchrone MFTs senden. Ein synchrones MFT sendet kein [metransformmarker](metransformmarker.md) -Ereignis als Antwort auf diese Meldung.

### <a name="implementation"></a>Implementierung

Asynchrone MFTs müssen wie beschrieben auf diese Meldung Antworten. Diese Meldung sollte durch synchrone MFTs ignoriert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MFT \_ - \_ Nachrichtentyp**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




