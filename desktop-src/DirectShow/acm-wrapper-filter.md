---
description: ACM-Wrapperfilter
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: ACM-Wrapperfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aaa56d955fe9cf1966e17c657fbf741b4bb8694a7f18b501b148b0383ea19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664079"
---
# <a name="acm-wrapper-filter"></a>ACM-Wrapperfilter

Mit dem ACM-Wrapperfilter können ACM-Codecs (Audio Compression Manager) einem Filterdiagramm beitreten. Er kann entweder als Dekomprimierungsfilter oder als Komprimierungsfilter fungieren.

Als Dekomprimierungsfilter wird der ACM-Wrapper in der Kategorie "DirectShow-Filter" (CLSID \_ LegacyAmFilterCategory) angezeigt und hat den Vorteil VON NORMAL \_ NORMAL. Der Verbindungsmedientyp auf dem Eingabepin bestimmt, welcher Codec vom Filter verwendet wird. In der Regel muss die Anwendung den Filter nicht dem Filterdiagramm hinzufügen. sie wird bei Bedarf automatisch vom Filter Graph Manager abgerufen. Die Dekomprimierung erfolgt nur für PCM-Audio.

Als Komprimierungsfilter wird der ACM-Wrapper in der Kategorie "Audio- und \_ AudioaudiocompressorCategory" (CLSID AudioCompressorCategory) angezeigt und verfügt über den Zusatz "NOT \_ \_ \_ USE". Jeder Codec wird als separate Instanz angezeigt. Für die Komprimierung können Sie den Filter nicht direkt mit CoCreateInstance erstellen. Stattdessen müssen Sie den Systemgeräte-Enumerator verwenden. Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filterschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Eingabepinmedientypen</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Eingabepinschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Medientypen des Ausgabepins</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Jede Kombination der folgenden Ist möglich:<br/>
<ul>
<li>Stichproben pro Sekunde (kHz): 44,1, 22,05, 11,025 oder 8,0.</li>
<li>Kanäle: Stereo oder Mono.</li>
<li>Bits pro Stichprobe: 8 oder 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ausgabepinschnittstellen</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtern von CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID der Eigenschaftenseite</td>
<td>Keine Eigenschaftenseite.</td>
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
<td><a href="filter-categories.md">Filterkategorie</a></td>
<td>CLSID_LegacyAmFilterCategory oder CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




