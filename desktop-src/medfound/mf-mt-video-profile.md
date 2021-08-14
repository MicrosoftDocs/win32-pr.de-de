---
description: Gibt das Profil der Videocodierung für den Ausgabemedientyp an. Dies ist ein Alias des MF \_ MT \_ MPEG2 \_ PROFILE-Attributs.
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2af7c6ebbbbb78626e96385a6eda5a25c38a3ae8473fac866866248570cc48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741393"
---
# <a name="mf_mt_video_profile-attribute"></a>MF \_ MT \_ VIDEO \_ PROFILE-Attribut

Gibt das Profil der Videocodierung für den Ausgabemedientyp an. Dies ist ein Alias des [MF \_ MT \_ MPEG2 \_ PROFILE-Attributs.](mf-mt-mpeg2-profile-attribute.md)

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

**H.264-Encoder:**

Unterstützte Profile werden überschritten und umfassen [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) und **eAVEncH264VProfile \_ ConstrainedHigh.**

Encoder müssen sowohl [**GetValue als**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) auch [**SetValue für**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) dieses Attribut unterstützen.

Dies ist statisch, daher müssen Videoencoder konfiguriert werden, bevor das Streaming gestartet wird. Wenn die Anwendung ein Profil fest legt, das vom Encoder nicht unterstützt wird, muss der Encoder den Medientyp ablehnen.

Empfohlener Standardwert: [**eAVEncH264VProfile-Hauptprofil. \_**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
