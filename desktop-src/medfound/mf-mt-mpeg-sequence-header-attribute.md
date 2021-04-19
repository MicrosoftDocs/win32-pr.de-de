---
description: Enthält den MPEG-1-oder MPEG-2-Sequenz Header für einen Video Medientyp.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350349"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>MF- \_ MT- \_ MPEG- \_ Sequenz \_ Header Attribut

Enthält den MPEG-1-oder MPEG-2-Sequenz Header für einen Video Medientyp.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut entspricht dem **dwsequenceheader** -Member der [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur oder dem **bsequenceheader** -Member der [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) -Struktur.

Im H264-und H265-Video enthält das BLOB verketteten [nal-Einheiten](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) im Anhang B-Format sowie die zugehörigen Start Codes. Speziell für H264 Video sind Sie SPS & PPS-nal-Einheiten. Für H265 sind Sie VPS, SPS & PPS.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
