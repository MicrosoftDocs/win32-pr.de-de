---
description: Gibt die maximale Makroblockverarbeitungsrate für einen H.264-Videostream an.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93bce2de0aa4f6c67cc7f6e61c09fde89923467a9211ba9e10642edf5a7f6416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104536"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>MF \_ MT \_ H264 \_ MAX MB PRO \_ \_ \_ SEKUNDE-Attribut

Gibt die maximale Makroblockverarbeitungsrate für einen H.264-Videostream an.

## <a name="data-type"></a>Datentyp

**UINT32 \[ \]** gespeichert als **UINT8 \[ \]**

## <a name="applies-to"></a>Gilt für:

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Medientypen für H.264-Streams, die über USB übertragen werden. Der Wert des Attributs ist ein Array von UINT32-Werten, die den folgenden Feldern im UVC 1.5 H.264-Videoformatdeskriptor entsprechen.

| Array-Element | Deskriptorfeld                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwMaxMBperSecOneResolutionNoScalability**                |
| 1             | **dwMaxMBperSecTwoResolutionsNoScalability**               |
| 2             | **dwMaxMBperSecThreeResolutionsNoScalability**             |
| 3             | **dwMaxMBperSecFourResolutionsNoScalability**              |
| 4             | **dwMaxMBperSecOneResolutionTemporalScalability**          |
| 5             | **dwMaxMBperSecTwoResolutionsTemporalScalablility**        |
| 6             | **dwMaxMBperSecThreeResolutionsTemporalScalability**       |
| 7             | **dwMaxMBperSecFourResolutionsTemporalScalability**        |
| 8             | **dwMaxMBperSecOneResolutionTemporalQualityScalability**   |
| 9             | **dwMaxMBperSecTwoResolutionsTemporalQualityScalability**  |
| 10            | **dwMaxMBperSecThreeResolutionsTemporalQualityScalablity** |
| 11            | **dwMaxMBperSecFourResolutionsTemporalQualityScalability** |
| 12            | **dwMaxMBperSecOneResolutionFullScalability**              |
| 13            | **dwMaxMBperSecTwoResolutionsFullScalability**             |
| 14            | **dwMaxMBperSecThreeResolutionsFullScalability**           |
| 15            | **dwMaxMBperSecFourResolutionsFullScalability**            |



 

Dieses Attribut wird auch mit [H.264 UVC 1.5-Kameraencodern](camera-encoder-h264-uvc-1-5.md)verwendet.

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

 

 




