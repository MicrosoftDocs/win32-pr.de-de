---
description: Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel gerade verarbeitet wird.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041909"
---
# <a name="mft_message_notify_start_of_stream"></a>\_Nachrichten \_ \_ Anfang \_ für \_ MFT-Nachricht Benachrichtigen

Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel gerade verarbeitet wird.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Bei synchronen MFTs ist es optional, diese Nachricht zu senden.

Für asynchrone MFTs muss der Client diese Nachricht senden.

### <a name="implementation"></a>Implementierung

Eine synchrone MFT ist nicht erforderlich, um auf die Meldung zu reagieren.

Diese Nachricht muss von einem asynchronen MFT implementiert werden, wie in [asynchronen MFTs](asynchronous-mfts.md)beschrieben.

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

 

 




