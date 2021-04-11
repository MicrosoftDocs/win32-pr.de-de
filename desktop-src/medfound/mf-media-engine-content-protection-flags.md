---
description: Gibt an, ob die Medien-Engine geschützte Inhalte wieder gibt.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351349"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>MF \_ - \_ \_ Attribut für Content \_ Protection \_ Flags für die MF-Medien

Gibt an, ob die Medien-Engine geschützte Inhalte wieder gibt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein bitweises **or** von-Flags aus der-Enumeration der [**MF-Medien-Engine- \_ \_ \_ \_ Schutzflags**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) . Um die Wiedergabe geschützter Inhalte zu aktivieren, legen Sie das Flag zum **\_ \_ \_ aktivieren \_ geschützter \_ Inhalte** für das MF-Medium fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>MF mediaengine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medien-Engine-Attribute](media-engine-attributes.md)
</dt> <dt>

[**IMF mediaengineclassfactory:: "forateinstance"**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




