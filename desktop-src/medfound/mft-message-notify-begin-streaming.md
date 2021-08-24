---
description: Benachrichtigt eine Media Foundation-Transformation (MFT), dass das Streaming beginnen wird.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491f84ee2dee752cccc251187c43bd497723a64ae6601954051f2aebab34ef85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848064"
---
# <a name="mft_message_notify_begin_streaming"></a>MFT \_ MESSAGE \_ NOTIFY \_ BEGIN \_ STREAMING

Benachrichtigt eine Media Foundation-Transformation (MFT), dass das Streaming beginnen wird.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Der Client muss diese Nachricht nicht senden. Wenn der Client diese Nachricht sendet, muss sie nach dem Festlegen aller Medientypen im MFT und vor dem Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)erfolgen. Der MFT kann reagieren, indem Puffer oder andere Ressourcen zugewiesen werden. Wenn der Client diese Nachricht nicht sendet, ordnet der MFT Ressourcen beim ersten Aufruf von **ProcessInput** zu. Daher kann das Senden dieser Nachricht die anfängliche Latenz reduzieren, wenn das Streaming beginnt.

### <a name="implementation"></a>Implementierung

Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




