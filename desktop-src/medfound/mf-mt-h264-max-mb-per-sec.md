---
description: Gibt die maximale Makroblock-Verarbeitungsrate für einen H. 264-Videostream an.
ms.assetid: 882F54D1-A963-4016-BEC7-F9C1AC5885FD
title: MF_MT_H264_MAX_MB_PER_SEC-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b53bdbabd9a633464ed388f2309627b69413c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347299"
---
# <a name="mf_mt_h264_max_mb_per_sec-attribute"></a>Attribut "MF \_ MT \_ H264 \_ Max \_ MB \_ pro \_ Sekunde"

Gibt die maximale Makroblock-Verarbeitungsrate für einen H. 264-Videostream an.

## <a name="data-type"></a>Datentyp

**\[ UInt32 \]** gespeichert als **Uint8 \[ \]**

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Medientypen für H. 264-Streams, die über USB übertragen werden. Der Wert des-Attributs ist ein Array von UInt32-Werten, die den folgenden Feldern im Videoformat Deskriptor UVC 1,5 H. 264 entsprechen.

| Array-Element | Deskriptorfeld                                           |
|---------------|------------------------------------------------------------|
| 0             | **dwmaxmbperseconeresolutionnoscalability**                |
| 1             | **dwmaxmbpersectworesolutionsnoscalability**               |
| 2             | **dwmaxmbpersecthreeresolutionsnoscalability**             |
| 3             | **dwmaxmbpersecfourresolutionsnoscalability**              |
| 4             | **dwmaxmbperseconeresolutiontemporalscalability**          |
| 5             | **dwmaxmbpersectworesolutionstemporalscalablility**        |
| 6             | **dwmaxmbpersecthreeresolutionstemporalscalability**       |
| 7             | **dwmaxmbpersecfourresolutionstemportscalability**        |
| 8             | **dwmaxmbperseconeresolutiontemporalqualityscalability**   |
| 9             | **dwmaxmbpersectworesolutionstemporalqualityscalability**  |
| 10            | **dwmaxmbpersecthreeresolutionstemporalqualityscalablity** |
| 11            | **dwmaxmbpersecfourresolutionstemporalqualityscalability** |
| 12            | **dwmaxmbperseconeresolutionfullscalability**              |
| 13            | **dwmaxmbpersectworesolutionsfullscalability**             |
| 14            | **dwmaxmbpersecthreeresolutionsfullscalability**           |
| 15            | **dwmaxmbpersecfourresolutionsfullscalability**            |



 

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

 

 




