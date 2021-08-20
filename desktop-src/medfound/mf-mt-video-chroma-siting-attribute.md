---
description: Beschreibt, wie Stichproben für einen YCbCr-Videomedientyp entnommen wurden.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: MF_MT_VIDEO_CHROMA_SITING-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5954f6d1649c366056bf9362a4226314d79ad78708fd4140f355506f7ee637d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741526"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>MF \_ MT VIDEO MF \_ \_ \_ SITING-Attribut

Beschreibt, wie Stichproben für einen Y'Cb'Cr'-Videomedientyp entnommen wurden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein bitweises **OR** von Flags aus der [**MFVideoColoraSubsampling-Enumeration.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Erweiterte Farbinformationen](extended-color-information.md)
</dt> </dl>

 

 




