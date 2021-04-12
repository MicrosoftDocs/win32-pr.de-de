---
description: Fordert eine Media Foundation Transformation (MFT) an, um das Streaming zu beenden.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527914"
---
# <a name="mft_message_notify_end_streaming"></a>MFT- \_ Nachrichten Nachrichten \_ Ende- \_ \_ Streaming

Fordert eine Media Foundation Transformation (MFT) an, um das Streaming zu beenden.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Der Client ist nicht verpflichtet, diese Nachricht zu senden, auch wenn der Client die Meldung zum Starten des Nachrichten Nachrichten dienstanterings zuvor gesendet hat. **\_ \_ \_ \_**

### <a name="implementation"></a>Implementierung

Die MFT kann auf diese Nachricht reagieren, indem Puffer und andere Ressourcen freigegeben werden. Die MFT leert keine Eingabedaten oder setzt die Medientypen als Reaktion auf diese Nachricht zurück. Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

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

 

 




