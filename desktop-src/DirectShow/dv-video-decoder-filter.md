---
description: DV-Video-Decoderfilter
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV-Video-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520464"
---
# <a name="dv-video-decoder-filter"></a>DV-Video-Decoderfilter

Mit diesem Filter wird ein Digital Video-Stream (DV) in ein unkomprimiertes Video decodiert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>iipdvdec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td><strong>Haupttyp</strong>: MEDIATYPE_Video<strong>Untertypen</strong>:<br/>
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
<strong>Format Typen</strong>:<br/> Format_VideoInfo Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
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
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**iipdvdec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) -Schnittstelle, um die Decodierungs Auflösung auf Full, halbsize, Quarter Size oder One-achte zu setzen.

**Interlacing**: in früheren Versionen des Decoders ist das Video immer Deinterlacing. Ab DirectX 9,0 kann der DV-Video Decoder das Interlacing beibehalten. Dadurch kann das Zeilen Sprung Video durch den Video Mischungs-Renderer (VMR) deinstalgt werden, um die renderingqualität zu verbessern. Um dieses Feature verwenden zu können, muss der downstreamfilter [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate unterstützen, die durch das Wert Format \_ VideoInfo2 im **Format Type** -Member der [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur "am" angegeben sind. Bei der Ausgabe der vollständigen Auflösung werden die Deinterlacing-Flags (**dwinterlace**) in der **VIDEOINFOHEADER2** -Struktur auf festgelegt `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , was Zeilen Sprung Felder angibt. Bei der Hälfte der Auflösung oder bei einem niedrigeren Wert ist **dwinterlace** auf 0 (null) festgelegt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




