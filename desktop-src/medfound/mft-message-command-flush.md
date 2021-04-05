---
description: Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753952"
---
# <a name="mft_message_command_flush"></a>MFT- \_ Nachrichten \_ Befehls Leerung \_

Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Nachdem diese Nachricht gesendet wurde, kann die MFT neue Eingabe Beispiele akzeptieren. Die aktuellen Medientypen werden nicht für ungültig erklärt.

### <a name="implementation"></a>Implementierung

Diese Nachricht muss von allen MFTs implementiert werden. Wenn diese Nachricht empfangen wird, sollte der MFT alle darin enthaltenen Medien Beispiele verwerfen.

[Asynchrone MFTs](asynchronous-mfts.md): der MFT sendet erst dann ein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, wenn eine Nachricht zum [**\_ \_ \_ Starten \_ des Nachrichten \_ Starts**](mft-message-notify-start-of-stream.md) vom Client empfangen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MFT \_ - \_ Nachrichtentyp**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




