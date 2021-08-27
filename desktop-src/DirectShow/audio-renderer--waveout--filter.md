---
description: Filter für Audiorenderer (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filter für Audiorenderer (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef79acb21221c1a0b91efc2da67773534fe54ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470157"
---
# <a name="audio-renderer-waveout-filter"></a>Filter für Audiorenderer (WaveOut)

Dieser Filter verwendet die \* waveOut-API, um Waveformaudio zu rendern. Der [DirectSound-Rendererfilter](directsound-renderer-filter.md) bietet jedoch die gleiche Funktionalität mit DirectSound. Standardmäßig verwendet der Filter Graph Manager anstelle dieses Filters den DirectSound-Renderer. Die Audiomischung ist im WaveOut-Audiorenderer deaktiviert. Wenn Sie also während der Wiedergabe mehrere Audiostreams mischen müssen, verwenden Sie den DirectSound-Renderer.

Dieser Filter überprüft nicht den Untertyp des Audiostreams. Die im Format [**übergebene WAVEFORMAT-**](/windows/win32/api/mmreg/ns-mmreg-waveformat) oder [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) enthält die für die Verbindung erforderlichen Informationen.

Dieser Filter unterstützt eine Reihe von Abtastraten, die vom Audiotreiber abhängen.




| | | Filterschnittstellen | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>Ipersiststream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | | Eingabepinmedientypen | <strong>MEDIATYPE_Audio</strong> | | Eingabepinschnittstellen | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | | Ausgabepinmedientypen | Nicht zutreffend. | | Ausgabepinschnittstellen | Nicht zutreffend. | | Filtern von CLSID-| <strong>CLSID_AudioRender</strong> | | CLSID-| der Eigenschaftenseite <strong>CLSID_AudioProperties</strong> <strong>, CLSID_AudioRendererAdvancedProperties</strong> | | Ausführbare | quartz.dll | | <a href="merit.md">Vorteile</a>  |  <strong>MERIT_DO_NOT_USE</strong> | | <a href="filter-categories.md">Filterkategorie</a>  |  <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 
