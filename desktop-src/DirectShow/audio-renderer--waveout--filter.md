---
description: Audiorendererfilter (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Audiorendererfilter (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66d92357b41b6fa23018acf6d44b966eb77fab
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987653"
---
# <a name="audio-renderer-waveout-filter"></a>Audiorendererfilter (WaveOut)

Dieser Filter verwendet die \* waveOut-API, um Waveformaudio zu rendern. Der [DirectSound-Rendererfilter](directsound-renderer-filter.md) bietet jedoch die gleiche Funktionalität mit DirectSound. Standardmäßig verwendet der Filter Graph-Manager den DirectSound-Renderer anstelle dieses Filters. Audiomischung ist im WaveOut Audio Renderer deaktiviert. Wenn Sie also während der Wiedergabe mehrere Audiostreams mischen müssen, verwenden Sie den DirectSound-Renderer.

Dieser Filter überprüft nicht den Untertyp des Audiostreams. Die [**im Format übergebene WAVEFORMAT-**](/windows/win32/api/mmreg/ns-mmreg-waveformat) oder [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) enthält die für die Verbindung erforderlichen Informationen.

Dieser Filter unterstützt eine Reihe von Beispielraten, die vom Audiotreiber abhängig sind.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSklave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>Ipersiststream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | 
| Eingabepin-Medientypen | <strong>MEDIATYPE_Audio</strong> | 
| Eingabepinschnittstellen | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | 
| Ausgabepin-Medientypen | Nicht zutreffend | 
| Ausgabe-PIN-Schnittstellen | Nicht zutreffend | 
| Filtern der CLSID | <strong>CLSID_AudioRender</strong> | 
| Eigenschaftenseite CLSID | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | <strong>MERIT_DO_NOT_USE</strong> | 
| <a href="filter-categories.md">Filterkategorie</a> | <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
