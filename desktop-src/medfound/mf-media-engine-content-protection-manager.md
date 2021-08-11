---
description: Ermöglicht der Medien-Engine die Wiedergabe geschützter Inhalte.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe80e619f3b256f6aa587f32d9ee5b6f43cd2978a5dfb043c62536ff5315bacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244689"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>MF \_ MEDIA ENGINE CONTENT PROTECTION \_ \_ \_ \_ MANAGER-Attribut

Ermöglicht der Medien-Engine die Wiedergabe geschützter Inhalte.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Zeiger auf die [**INTERFACESContentProtectionManager-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) Der Aufrufer muss die -Schnittstelle implementieren.

Dieses Attribut kann eines der Attribute sein, die an [**DIE ATTRIBUTEMEDIAEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)übergeben werden. Er ist erforderlich, wenn geschützter Inhalt wiedergegeben werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ADRMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




