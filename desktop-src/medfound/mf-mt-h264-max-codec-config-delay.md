---
description: Die maximale Anzahl von Frames, die der H. 264-Encoder benötigt, um auf einen Befehl zu antworten.
ms.assetid: C856B2B0-4A06-436D-B589-B01DA86DB53D
title: MF_MT_H264_MAX_CODEC_CONFIG_DELAY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a835d5b5a37be0c722f313aaf4fe8ed8aa55f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362413"
---
# <a name="mf_mt_h264_max_codec_config_delay-attribute"></a>"MF \_ MT \_ H264 \_ Max \_ Codec \_ config Delay \_ "-Attribut

Die maximale Anzahl von Frames, die der H. 264-Encoder benötigt, um auf einen Befehl zu antworten.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden. Der Wert entspricht dem Feld **bmaxcodecconfigdelay** im Videoformat Deskriptor UVC 1,2 H. 264.

Dieses Attribut wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




