---
description: Die maximale Anzahl von Frames, die der H.264-Encoder benötigt, um auf einen Befehl zu reagieren.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: MF_MT_H264_MAX_CODEC_CONFIG_DELAY -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc3610f9fce8201e3381b9684e3ea5b76578d8a22f751821dd16b0d9742ffff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035198"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a>MF \_ MT \_ H264 \_ MAX CODEC \_ \_ CONFIG \_ DELAY-Attribut

Die maximale Anzahl von Frames, die der H.264-Encoder benötigt, um auf einen Befehl zu reagieren.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medientypen für H.264-Streams, die über USB übertragen werden. Der Wert entspricht dem **Feld bMaxCodecConfigDelay** im Videoformatdeskriptor UVC 1.2 H.264.

Dieses Attribut wird auch mit [H.264 UVC 1.5-Kameraencodern verwendet.](camera-encoder-h264-uvc-1-5.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




