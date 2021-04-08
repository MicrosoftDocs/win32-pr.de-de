---
description: DV-Video Encoder-Filter
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV-Video Encoder-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957762"
---
# <a name="dv-video-encoder-filter"></a>DV-Video Encoder-Filter

Mit diesem Filter wird ein unkomprimierter Videostream in ein digitales Video (DV) codiert. Sie stellt eine benutzerdefinierte Schnittstelle ( [**idvenc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)) zum Festlegen der Codierungs Auflösung und des Codierungs Formats bereit.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>idvenc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td><ul>
<li>Haupttyp: MEDIATYPE_VideoThe folgenden Untertypen sind gültig:<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>Formattyp: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td><ul>
<li>Haupttyp: MEDIATYPE_Video</li>
<li>Untertyp: MEDIASUBTYPE_dvsd</li>
<li>Formattyp: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Bei einem 16-Bit-Video (mediasubtype \_ RGB555 oder mediasubtype \_ RGB565) müssen die Eingaben 720 x 480 Pixel für NTSC oder 720 x 576 Pixel für PAL lauten. Bei 24-Bit-Videos gibt es keine Größenbeschränkungen für die Eingabe.

Die Ausgabe lautet immer 720 x 480 für NTSC oder 720 x 576 für PAL; 24-Bit-Video wird so skaliert, dass diese Dimensionen angepasst werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




