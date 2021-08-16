---
description: Gibt den Ratensteuerungsmodus für einen H.264-Videostream an.
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: MF_MT_H264_RATE_CONTROL_MODES-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34fac6f047b8454ea6ddd79dfd26659fa7751fd1a6a14e01c7ea9457a5f7dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104436"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a>MF \_ MT \_ H264 \_ RATE CONTROL \_ \_ MODES-Attribut

Gibt den Ratensteuerungsmodus für einen H.264-Videostream an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medientypen für H.264-Streams, die über USB übertragen werden. Der Wert entspricht dem **bmRateControlModes-Feld** im UVC 1.2 H.264-Test-/Commit-Steuerelement.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




