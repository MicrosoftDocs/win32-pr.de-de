---
description: Gibt an, ob die Medien-Engine geschützte Inhalte wiedergibt.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS -Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956440"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>MF \_ MEDIA ENGINE CONTENT PROTECTION \_ \_ \_ \_ FLAGS-Attribut

Gibt an, ob die Medien-Engine geschützte Inhalte wiedergibt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein bitweises **OR** von Flags aus der [**MF \_ MEDIA ENGINE \_ PROTECTION \_ \_ FLAGS-Enumeration.**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) Um die Wiedergabe geschützter Inhalte zu aktivieren, legen Sie das **Flag MF \_ MEDIA ENGINE ENABLE PROTECTED \_ \_ \_ \_ CONTENT** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medien-Engine-Attribute](media-engine-attributes.md)
</dt> <dt>

[**ÄNDERMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




