---
description: Gibt das Profil der Videocodierung für den Ausgabe Medientyp an. Dies ist ein Alias des MF \_ MT \_ \_
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364235"
---
# <a name="mf_mt_video_profile-attribute"></a>MF \_ MT- \_ Video \_ Profil Attribut

Gibt das Profil der Videocodierung für den Ausgabe Medientyp an. Dies ist ein Alias des [MF \_ MT \_ \_ ](mf-mt-mpeg2-profile-attribute.md)

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

**H. 264-Encoder:**

Unterstützte Profile werden mit [**eAVEncH264VProfile \_ einschränieedbase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) und **eAVEncH264VProfile \_ einschräninedhigh** überschritten.

Encoder müssen sowohl [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) als auch [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) für dieses Attribut unterstützen.

Dies ist statisch, sodass Video Encoder konfiguriert werden müssen, bevor das Streaming gestartet wird. Wenn von der Anwendung ein Profil festgelegt wird, das der Encoder nicht unterstützt, lehnt der Encoder den Medientyp ab.

Empfohlene Standardeinstellung: [**eAVEncH264VProfile \_ Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) Profile.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
