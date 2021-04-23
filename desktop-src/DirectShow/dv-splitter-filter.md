---
description: DV-Splitterfilter
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: DV-Splitterfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ca8e856f1a49ff22ee05f7dc0ae341fad6aa91
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908408"
---
# <a name="dv-splitter-filter"></a>DV-Splitterfilter

Dieser Filter teilt einen überlappten digitalen Videodatenstrom (DV) in seine Komponentenvideo- und Audiostreams auf.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Eingabepin-Medientypen                    | MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                                         |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabepin-Medientypen                   | **Video**: MEDIATYPE \_ Video, FORMAT \_ DvInfo<br/> **Audio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx<br/>             |
| Ausgabe-PIN-Schnittstellen                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                                                                  |
| Ausführbare Datei                               | qdv.dll                                                                                                                                            |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                      |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

DV-Frames enthalten Audio und Video in demselben Frame. Der DV-Splitterfilter extrahiert die Audiodaten und übermittelt sie als einen oder zwei Audiostreams aus den Audioausgabepins. Der ursprüngliche DV-Frame wird vom Videoausgabepin als Videoframe übermittelt. Der Medientyp im Videoframe wird von MEDIATYPE \_ Interleaved in MEDIATYPE \_ Video geändert, andernfalls werden die Daten jedoch nicht geändert. Der Medientyp wird geändert, um zu signalisieren, dass die Audiodaten im Frame ignoriert werden sollen. Der DV-Splitter legt keine Medienzeit für die Ausgabebeispiele fest. Wenn Sie einen Downstreamfilter schreiben, der die Medienzeiten erfordert, können Sie die Zeiten von der Frameanzahl ableiten.

Nur jeweils ein Ausgabepin macht die Schnittstellen [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) verfügbar.

Der DV-Splitterfilter kann dynamische Formatänderungen im Audiostream akzeptieren. Wenn der [AVI Mux-Filter](avi-mux-filter.md) jedoch nachgeschaltet ist, lehnt er die Formatänderung ab. In diesem Fall erzeugt der DV-Splitter keine Audiodatenströme mehr. Diese Einschränkung wirkt sich nur auf die Dateierfassung vom Typ 2 aus. Bei Dateien vom Typ 1 wird der überlappende Stream nicht von Anfang an aufgeteilt. Für die Vorschau ist kein AVI Mux-Filter nachgeschaltet.

Wenn es sich bei der DV-Quelle um eine Livekamera handelt, gibt es normalerweise keinen Grund, das Audioformat zu ändern. Das Format kann sich jedoch ändern, wenn Sie von einem VTR-Band übertragen, das mehrere heterogene Quellen enthält.

Jeder DV-Frame enthält zusätzlich zu den Audio- und Videodaten Metadaten. Diese Metadaten können sich von Frame zu Frame ändern. Anwendungen können die Metadaten analysieren, indem sie entweder die Eingabebeispiele oder die Videoausgabebeispiele untersuchen. DirectShow bietet jedoch keine direkte Unterstützung für die Analyse von DV-Metadaten. Weitere Informationen finden Sie unter IEC 61834-4.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




