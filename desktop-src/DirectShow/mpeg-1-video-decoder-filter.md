---
description: MPEG-1-Videodecoderfilter
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: MPEG-1-Videodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468227"
---
# <a name="mpeg-1-video-decoder-filter"></a>MPEG-1-Videodecoderfilter

Decodiert MPEG-1-Video.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Eingabepin-Medientypen | MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Die folgenden Untertypen sind gültig:<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin | |</strong></a> Ausgabepin-Medientypen | Haupttyp: <strong>MEDIATYPE_Video</strong>,<br /> Formattyp: <strong>FORMAT_VideoInfo</strong> oder <strong>FORMAT_VideoInfo2</strong><br /> Untertypen:<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Filtern von CLSID-| <strong>CLSID_CMpegVideoCodec</strong> | | CLSID-Eigenschaftsseite | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | Ausführbare | quartz.dll | | <a href="merit.md">Leistungs-|</a> 0x40000001 | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Hinweise

Dieser Filter kann in eine DirectDraw-Oberfläche decodiert werden. Der Filter verwendet MMX, wenn der Computer MMX unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




