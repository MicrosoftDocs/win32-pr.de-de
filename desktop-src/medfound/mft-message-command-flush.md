---
description: 'MFT_MESSAGE_COMMAND_FLUSH: Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35363e376c9c6bd5de6ee9dcef9eac86901232f964eb11773fcd76bbf6280282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689038"
---
# <a name="mft_message_command_flush"></a>MFT \_ MESSAGE \_ COMMAND \_ FLUSH

Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Nachdem diese Nachricht gesendet wurde, kann der MFT neue Eingabebeispiele akzeptieren. Die aktuellen Medientypen werden nicht ungültig.

### <a name="implementation"></a>Implementierung

Alle MFTs müssen diese Meldung implementieren. Wenn diese Meldung empfangen wird, sollte der MFT alle Medienbeispiele verwerfen, die er enthält.

[Asynchrone MFTs:](asynchronous-mfts.md)Der MFT sendet kein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) bis er eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




