---
description: Gibt die Funktionen-Flags für einen H. 264-Videostream an.
ms.assetid: 59EF18D6-6063-4EF3-BBFB-51A966CFF09E
title: MF_MT_H264_CAPABILITIES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67f796e09d4b57667a3d8f7c7c0fa888eba7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868552"
---
# <a name="mf_mt_h264_capabilities-attribute"></a>MF \_ MT \_ H264- \_ Funktionen-Attribut

Gibt die Funktionen-Flags für einen H. 264-Videostream an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden. Der Wert entspricht dem Feld **bmfunktionen** im Video Frame Deskriptor UVC 1,5 H. 264.

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

 

 




