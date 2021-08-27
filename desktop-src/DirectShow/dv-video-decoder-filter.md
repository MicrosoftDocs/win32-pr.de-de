---
description: DV-Videodecoderfilter
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV-Videodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12131aa09f8e3f7dbef56504ad55410af11ffcbe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466047"
---
# <a name="dv-video-decoder-filter"></a>DV-Videodecoderfilter

Dieser Filter decodiert einen digitalen Videodatenstrom (DV) in unkomprimiertes Video.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong> | | Eingabepin-Medientypen | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo, FORMAT_DvInfo</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Ausgabepin-Medientypen | <strong>Haupttyp:</strong>MEDIATYPE_Video<strong>Untertypen:</strong><br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>Formattypen:</strong><br /> Format_VideoInfo, Format_VideoInfo2<br /> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Filtern von CLSID-| CLSID_DVVideoCodec | | CLSID-Eigenschaftsseite | CLSID_DVDecPropertiesPage | | Ausführbare | qdv.dll | | <a href="merit.md">Leistungs-|</a> MERIT_NORMAL | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Hinweise

Verwenden Sie [**die IIPDVDec-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) um die Decodierungsauflösung auf full, half size, quarter size oder one-achte Größe zu setzen.

**Interlacing:** Frühere Versionen des Decoders deinterlacen das Video immer. Ab DirectX 9.0 kann der DV-Videodecoder das Interlacing beibehalten. Dadurch kann das geschachtelte Video durch den Video Mixing Renderer (VMR) deinterlaced werden, um die Renderingqualität zu verbessern. Um dieses Feature verwenden zu können, muss der Downstreamfilter [**VIDEOINFOHEADER2-Formate**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) unterstützen, die durch den Wert Format \_ VideoInfo2 im **formattype-Member** der [**AM MEDIA \_ \_ TYPE-Struktur angegeben**](/windows/win32/api/strmif/ns-strmif-am_media_type) werden. Bei der Ausgabe der vollständigen Auflösung werden die Deinterlacingflags (**dwInterlace**) in der **VIDEOINFOHEADER2-Struktur** auf festgelegt, was `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` interlaced-Felder angibt. Bei halber Auflösung oder niedriger ist **dwInterlace** auf 0 (null) festgelegt, was progressive Frames angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




