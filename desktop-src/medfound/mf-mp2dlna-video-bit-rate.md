---
description: Gibt die maximale Video Bitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215148"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>MF \_ MP2DLNA \_ Video \_ \_ Bitrate-Attribut

Gibt die maximale Video Bitrate für die DLNA-Medien Senke (Digital Living Network Alliance) an.

## <a name="data-type"></a>Datentyp

**UINT32**

Der Wert ist die maximale Zielbitrate für den codierten Videostream (in Bits pro Sekunde). Der Höchstwert beträgt 9,8 Millionen (9,8 Mbit/s), der auch der Standardwert ist.

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab. Legen Sie das-Attribut vor Beginn des Streamings fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




