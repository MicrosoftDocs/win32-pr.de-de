---
description: Fordert eine Media Foundation-Transformation (MFT) an, damit das Streaming beendet wird.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae36412a35dd142efab89f17827b1c9cb6475494ff88f8af800bd8fee65d456f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871964"
---
# <a name="mft_message_notify_end_streaming"></a>MFT \_ MESSAGE \_ NOTIFY \_ END \_ STREAMING

Fordert eine Media Foundation-Transformation (MFT) an, damit das Streaming beendet wird.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Der Client muss diese Nachricht nicht senden, auch wenn der Client zuvor die **MFT \_ MESSAGE NOTIFY \_ BEGIN \_ \_ STREAMING-Nachricht** gesendet hat.

### <a name="implementation"></a>Implementierung

Der MFT kann auf diese Nachricht reagieren, indem Puffer und andere Ressourcen freigegeben werden. Der MFT leert keine Eingabedaten und setzt die Medientypen nicht als Reaktion auf diese Nachricht zurück. Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

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

 

 




