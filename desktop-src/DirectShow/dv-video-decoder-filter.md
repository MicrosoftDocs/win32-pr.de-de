---
description: DV-Videodecoderfilter
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV-Videodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f00d63c92da4c16697d7cc9ff173f4c50e822a10da429a586f8eaa688e9eb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820682"
---
# <a name="dv-video-decoder-filter"></a>DV-Videodecoderfilter

Dieser Filter decodiert einen digitalen Videodatenstrom (DV) in unkomprimiertes Video.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filterschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Eingabepin-Medientypen</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo, FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eingabepinschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabepin-Medientypen</td>
<td><strong>Haupttyp:</strong>MEDIATYPE_Video<strong>Untertypen:</strong><br/>
<ul>
<li>MEDIASUBTYPE_YUY2</li>
<li>MEDIASUBTYPE_UYVY</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
<li>MEDIASUBTYPE_ARGB32</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_Y41P</li>
</ul>
<strong>Formattypen:</strong><br/> Format_VideoInfo, Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>Ausgabe-PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtern der CLSID</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>Eigenschaftenseite CLSID</td>
<td>CLSID_DVDecPropertiesPage</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filterkategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Verwenden Sie [**die IIPDVDec-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) um die Decodierungsauflösung auf full, half size, quarter size oder one-achte Größe zu setzen.

**Interlacing:** Frühere Versionen des Decoders deinterlacen das Video immer. Ab DirectX 9.0 kann der DV-Videodecoder das Interlacing beibehalten. Dadurch kann das geschachtelte Video durch den Video Mixing Renderer (VMR) deinterlaced werden, um die Renderingqualität zu verbessern. Um dieses Feature verwenden zu können, muss der Downstreamfilter [**VIDEOINFOHEADER2-Formate**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) unterstützen, die durch den Wert Format \_ VideoInfo2 im **formattype-Member** der [**AM MEDIA \_ \_ TYPE-Struktur angegeben**](/windows/win32/api/strmif/ns-strmif-am_media_type) werden. Bei der Ausgabe der vollständigen Auflösung werden die Deinterlacingflags (**dwInterlace**) in der **VIDEOINFOHEADER2-Struktur** auf festgelegt, was `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` interlaced-Felder angibt. Bei halber Auflösung oder niedriger ist **dwInterlace** auf 0 (null) festgelegt, was progressive Frames angibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




