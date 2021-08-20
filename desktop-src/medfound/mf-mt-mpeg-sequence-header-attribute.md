---
description: Enthält den MPEG-1- oder MPEG-2-Sequenzheader für einen Videomedientyp.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: MF_MT_MPEG_SEQUENCE_HEADER Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e988a5b64b7b1c99d3c84de7441f492cebe07f0b473ee3f5256c732fbb7697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035148"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a>MF \_ MT MPEG SEQUENCE \_ \_ \_ HEADER-Attribut

Enthält den MPEG-1- oder MPEG-2-Sequenzheader für einen Videomedientyp.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Hinweise

Dieses Attribut entspricht dem **dwSequenceHeader-Member** der [**MPEG2VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) oder dem **bSequenceHeader-Member** der [**MPEG1VIDEOINFO-Struktur.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)

Für h264- und h265-Videos enthält das Blob verkettete [NAL-Einheiten](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) im Format Anhang B zusammen mit ihren Startcodes. Insbesondere für h264-Videos handelt es sich um SPS-& PPS-NAL-Einheiten. Bei h265 handelt es sich um VPS, SPS & PPS.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
