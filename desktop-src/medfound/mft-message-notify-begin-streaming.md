---
description: Benachrichtigt eine Media Foundation Transform (MFT), dass das Streaming im Begriff ist.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215035"
---
# <a name="mft_message_notify_begin_streaming"></a>MFT- \_ Nachrichten \_ Benachrichtigung zum Starten des \_ \_ Streamings

Benachrichtigt eine Media Foundation Transform (MFT), dass das Streaming im Begriff ist.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Der Client muss diese Nachricht nicht senden. Wenn der Client diese Nachricht sendet, muss dies nach dem Festlegen aller Medientypen auf der MFT und vor dem Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)durchgeführt werden. Die MFT kann Antworten, indem Puffer oder andere Ressourcen zugeordnet werden. Wenn der Client diese Nachricht nicht sendet, ordnet der MFT beim ersten Aufrufen von **ProcessInput** Ressourcen zu. Daher kann das Senden dieser Nachricht die anfängliche Latenz verringern, wenn das Streaming beginnt.

### <a name="implementation"></a>Implementierung

Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

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

 

 




