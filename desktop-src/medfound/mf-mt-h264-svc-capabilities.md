---
description: Gibt die SVC-Funktionen eines H.264-Videostreams an.
ms.assetid: B727D9D2-6126-41F8-A27A-743640FE3AE4
title: MF_MT_H264_SVC_CAPABILITIES-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e99e1739b7c39d884165f56c54f87128fdf2cc02fbaab75dff15a4d21f1656
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035158"
---
# <a name="mf_mt_h264_svc_capabilities-attribute"></a>MF \_ MT \_ H264 \_ SVC \_ CAPABILITIES-Attribut

Gibt die SVC-Funktionen eines H.264-Videostreams an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medientypen für H.264-Streams, die über USB übertragen werden. Der Wert entspricht dem **BmSVCCapabilities-Feld** im UVC 1.5 H.264-Videoframedeskriptor.

Dieses Attribut wird auch mit [H.264 UVC 1.5-Kameraencodern](camera-encoder-h264-uvc-1-5.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




