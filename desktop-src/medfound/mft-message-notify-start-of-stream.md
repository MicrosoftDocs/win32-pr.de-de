---
description: Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel verarbeitet wird.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973029"
---
# <a name="mft_message_notify_start_of_stream"></a>MFT \_ MESSAGE \_ NOTIFY \_ START \_ OF \_ STREAM

Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel verarbeitet wird.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen [**Sie DIETRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Bei synchronen MFTs ist es optional, diese Nachricht zu senden.

Bei asynchronen MFTs muss der Client diese Nachricht senden.

### <a name="implementation"></a>Implementierung

Eine synchrone MFT ist nicht erforderlich, um auf die Nachricht zu reagieren.

Eine asynchrone MFT muss diese Meldung implementieren, wie unter [Asynchrone MFTs beschrieben.](asynchronous-mfts.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




