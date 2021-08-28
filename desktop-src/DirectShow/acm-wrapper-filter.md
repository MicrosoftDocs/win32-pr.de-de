---
description: ACM-Wrapperfilter
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: ACM-Wrapperfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985353"
---
# <a name="acm-wrapper-filter"></a>ACM-Wrapperfilter

Mit dem ACM-Wrapperfilter können ACM-Codecs (Audio Compression Manager) einem Filterdiagramm beitreten. Sie kann entweder als Dekomprimierungsfilter oder als Komprimierungsfilter fungieren.

Als Dekomprimierungsfilter wird der ACM-Wrapper in der Kategorie "DirectShow-Filter" (CLSID LegacyAmFilterCategory) angezeigt und hat einen Vorteil von \_ NORMAL \_ NORMAL. Der Verbindungsmedientyp auf dem Eingabepin bestimmt, welcher Codec vom Filter verwendet wird. In der Regel muss die Anwendung den Filter nicht dem Filterdiagramm hinzufügen. Sie wird bei Bedarf automatisch vom Filter Graph Manager eingezogen. Die Dekomprimierung wird nur für PCM-Audiodaten verwendet.

Als Komprimierungsfilter wird der ACM-Wrapper in der Kategorie "Audio Audio \_ AudioCompressorCategory" (CLSID AudioCompressorCategory) angezeigt und hat den Vorteil, DASS SIE NICHT \_ \_ \_ VERWENDEN. Jeder Codec wird als separate Instanz angezeigt. Für die Komprimierung können Sie den Filter nicht direkt mit CoCreateInstance erstellen. Stattdessen müssen Sie den Systemgeräte-Enumerator verwenden. Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).




| Bezeichnung | Wert |
|--------|-------|
| Filtern von Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag | 
| Eingabepin-Medientypen | MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Jede Kombination der folgenden Sind möglich:<br /><ul><li>Stichproben pro Sekunde (kHz): 44,1, 22,05, 11,025 oder 8,0.</li><li>Kanäle: Stereo oder Mono.</li><li>Bits pro Beispiel: 8 oder 16.</li></ul> | 
| Schnittstellen für Ausgabepins | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern der CLSID | CLSID_ACMWrapper | 
| Eigenschaftenseite CLSID | Keine Eigenschaftenseite. | 
| Ausführbare Datei | Quartz.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_NORMAL oder MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory oder CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




