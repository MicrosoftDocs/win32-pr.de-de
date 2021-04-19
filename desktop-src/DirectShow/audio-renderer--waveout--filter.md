---
description: Filter für audiorenderer (waveout)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filter für audiorenderer (waveout)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346612"
---
# <a name="audio-renderer-waveout-filter"></a>Filter für audiorenderer (waveout)

Dieser Filter verwendet die waveout \* -API zum Rendering von Wellenform-Audiodaten. Der [DirectSound-rendererfilter](directsound-renderer-filter.md) bietet jedoch die gleiche Funktionalität mithilfe von DirectSound. Standardmäßig verwendet der Filter Graph-Manager den DirectSound-Renderer anstelle dieses Filters. Die Audiomischung ist im waveout-audiorenderer deaktiviert. Wenn Sie also mehrere Audiostreams während der Wiedergabe mischen müssen, verwenden Sie den DirectSound-Renderer.

Dieser Filter überprüft den Untertyp des Audiostreams nicht. Die im Format übergebenen [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -oder [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur enthält die Informationen, die für die Verbindung erforderlich sind.

Dieser Filter unterstützt eine Reihe von Stichproben Raten, die vom Audiotreiber abhängig sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Iamaudiorendererstats</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>Iamclockslave</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>Iamdirectsound</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>Iamresourcecontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>Ibasicaudiodatei</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li>
<li>IPersistPropertyBag</li>
<li>IPersistStream</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td><strong>MEDIATYPE_Audio</strong></td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td><strong>CLSID_AudioRender</strong></td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td><strong>CLSID_AudioProperties</strong> <strong>CLSID_AudioRendererAdvancedProperties</strong></td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
