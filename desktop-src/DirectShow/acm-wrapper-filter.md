---
description: ACM-Wrapper Filter
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: ACM-Wrapper Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338880"
---
# <a name="acm-wrapper-filter"></a>ACM-Wrapper Filter

Mit dem ACM-Wrapper Filter können ACM-Codecs (Audiokomprimierungs-Manager) einem Filter Diagramm beitreten. Er kann entweder als Filter für die herab Komprimierung oder als Komprimierungs Filter fungieren.

Als Filter für die Komprimierung wird der ACM-Wrapper in der Kategorie "DirectShow-Filter" (CLSID \_ legacyamfiltercategory) angezeigt, und es ist ein Verdienst des Werts " \_ Normal". Der Typ der Verbindungs Medien in der Eingabe-PIN bestimmt, welcher Codec vom Filter verwendet wird. In der Regel muss die Anwendung dem Filter Diagramm den Filter nicht hinzufügen. Sie wird automatisch vom Filter Graph-Manager abgerufen, wenn dies erforderlich ist. Die Komprimierung erfolgt nur für PCM-Audiodaten.

Als Komprimierungs Filter wird der ACM-Wrapper in der Kategorie "Audio-Kompressoren" (CLSID \_ audiocompressorcategory) angezeigt, und es wird \_ die \_ \_ Nutzung nicht verwendet. Jeder Codec wird als separate Instanz angezeigt. Zur Komprimierung können Sie den Filter nicht direkt mit cokreatanstance erstellen. Stattdessen müssen Sie den Enumerator für Systemgeräte verwenden. Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filter Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, ipersistent, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Eingabe-PIN-Medientypen</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>PIN-Eingabeschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>Ausgabe-PIN-Medientypen</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. eine beliebige Kombination der folgenden Möglichkeiten ist möglich:<br/>
<ul>
<li>Stichproben pro Sekunde (kHz): 44,1, 22,05, 11,025 oder 8,0.</li>
<li>Kanäle: Stereo oder Mono.</li>
<li>Bits pro Stichprobe: 8 oder 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PIN-Schnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>Iamstreamconfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaften Seite</td>
<td>Keine Eigenschaften Seite.</td>
</tr>
<tr class="even">
<td>Ausführbare Datei</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td>MERIT_NORMAL oder MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Filter Kategorie</a></td>
<td>CLSID_LegacyAmFilterCategory oder CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




