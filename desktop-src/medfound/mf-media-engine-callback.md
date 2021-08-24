---
description: Enthält einen Zeiger auf die Rückrufschnittstelle für die Medien-Engine.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: MF_MEDIA_ENGINE_CALLBACK -Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ba6149c8d0b615ad13277588bbee5ee7397d9adaa089195671b3336b2b406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723043"
---
# <a name="mf_media_engine_callback-attribute"></a>MF \_ MEDIA \_ ENGINE \_ CALLBACK-Attribut

Enthält einen Zeiger auf die Rückrufschnittstelle für die Medien-Engine.

## <a name="data-type"></a>Datentyp

**ÄNDERMediaEngineNotify \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DANNATTRIBUTEs::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die VON der Anwendung implementierte [**BERMEDIAEngineNotify-Schnittstelle.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)

Dieses Attribut wird zusammen mit der [**METHODE FÜR DIETMEDIAEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) verwendet, um die Medien-Engine zu initialisieren. Das -Attribut ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ÄNDERMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[**ÄNDERMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




