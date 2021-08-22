---
description: Ungefähre Datenrate des Videodatenstroms in Bits pro Sekunde für einen Videomedientyp.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: MF_MT_AVG_BITRATE-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88ae74eafa9542e42a6def6f25c8bb0fbf3675c320b3e0760c17a40388885ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664270"
---
# <a name="mf_mt_avg_bitrate-attribute"></a>MF \_ MT \_ AVG \_ BITRATE-Attribut

Ungefähre Datenrate des Videodatenstroms in Bits pro Sekunde für einen Videomedientyp.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut entspricht dem **dwBitRate-Member** der [**VIDEOINFOHEADER-**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und [**VIDEOINFOHEADER2-Strukturen.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
