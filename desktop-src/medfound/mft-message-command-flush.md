---
description: 'MFT_MESSAGE_COMMAND_FLUSH: Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092738"
---
# <a name="mft_message_command_flush"></a>MFT \_ MESSAGE \_ COMMAND \_ FLUSH

Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Nachdem diese Nachricht gesendet wurde, kann der MFT neue Eingabebeispiele akzeptieren. Die aktuellen Medientypen werden nicht ungültig.

### <a name="implementation"></a>Implementierung

Alle MFTs müssen diese Nachricht implementieren. Wenn diese Nachricht empfangen wird, sollte der MFT alle Medienbeispiele verwerfen, die er enthält.

[Asynchrone MFTs:](asynchronous-mfts.md)Der MFT sendet kein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) bis er eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




