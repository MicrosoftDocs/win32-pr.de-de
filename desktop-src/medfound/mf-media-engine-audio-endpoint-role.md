---
description: Gibt die Geräte Rolle für den Audiodatenstrom an.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106369928"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>\_ \_ \_ Audioendpunkt- \_ \_ Rollen Attribut der MF-Medien-Engine

Gibt die Geräte Rolle für den Audiodatenstrom an.

## <a name="data-type"></a>Datentyp

**[**Erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** als **UInt32** gespeichert

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration.

Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren. Das-Attribut ist optional.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
