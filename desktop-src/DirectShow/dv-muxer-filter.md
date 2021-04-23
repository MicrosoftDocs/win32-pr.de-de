---
description: DV Muxer-Filter
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908598"
---
# <a name="dv-muxer-filter"></a>DV Muxer-Filter

Dieser Filter kombiniert ein digitales Video (DV) – codierter Videodatenstrom mit einem oder zwei Audiostreams, um einen überlappende DV-Datenstrom zu erzeugen. Um den Stream in eine AVI-Datei zu schreiben, verbinden Sie diesen Filter mit dem [AVI Mux-Filter](avi-mux-filter.md) und den *AVI Mux* mit dem [File Writer-Filter.](file-writer-filter.md) Weitere Informationen finden Sie unter [Digitales Video in DirectShow.](digital-video-in-directshow.md)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Eingabe-Stecknadelmedientypen                    | **Video**: MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio**: MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                             |
| Ausgabe-Pin-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| Filtern von CLSID                             | CLSID \_ DVMux                                                                                                                           |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                       |
| Ausführbare Datei                               | qdv.dll                                                                                                                                |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                                                        |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Der DV Muxer kann zwei Audioeingabepins erstellen. Sie unterstützt die in der folgenden Tabelle gezeigten Audioformate.



Audiopin 1

Audiopin 2

Ausgabeformat

Abtastrate (kHz)

Bits/Beispiel

Channels

Samplingrate

Bits/Beispiel

Channels

32

16

Mono

Unverbunden

SD 2-Kanal

32

16

Stereo

Unverbunden

SD 4-Kanal

44.1 oder 48

16

Stereo oder Mono

Unverbunden

SD 2-Kanal

Unverbunden

32

16

Stereo oder Mono

Unzulässig

Unverbunden

44.1 oder 48

16

Mono

Unzulässig

Unverbunden

44.1 oder 48

16

Stereo

SD 2-Kanal

32

16

Mono

32

16

Mono

SD 2-Kanal

32

16

Stereo oder Mono\*

32

16

Stereo oder Mono\*

SD 4-Kanal

44.1

16

Mono

44.1

16

Mono

SD 2-Kanal

48

16

Mono

48

16

Mono

SD 2-Kanal

\* Wenn mindestens ein Eingabepin stereo ist.



 

Für diese Tabelle wird Audiopin 1 als erster Eingabepin definiert, der mit einer Audioquelle verbunden ist, und Audiopin 2 ist als zweiter Eingabepin definiert, der mit einer Audioquelle verbunden ist. Sobald eine Audiostecknadel verbunden ist, bleibt dieses Nummerierungsschema wirksam, es sei denn, beide Audiopins werden getrennt. Wenn Sie beispielsweise beide Audiopins verbinden und dann audio pin 1 trennen, wird der verbleibende Pin weiterhin als Pin 2 betrachtet.

Audiodaten, die an Pin 1 übermittelt werden, werden im ersten Audioblock der DV-Frames (CH1) aufgezeichnet, und Audiodaten, die an Pin 2 übermittelt werden, werden im zweiten Audioblock (CH2) aufgezeichnet. Ausnahme: Wenn der Filter über eine einzelne Stereoeingabe mit 44,1 kHz oder 48 kHz verfügt, wird der linke Audiokanal im ersten Audioblock aufgezeichnet, und der rechte Audiokanal wird im zweiten Audioblock aufgezeichnet.

Für SD 4-Kanal-Ausgabe: Wenn die Eingabe Stereo ist, wird die linke Spur in CHa oder CHc aufgezeichnet, und die rechte Spur wird in CHb oder CHd aufgezeichnet. Wenn die Eingabe mono ist, wird die Audiodatei in CHa oder CHc aufgezeichnet, und CHb und CHd sind im Hintergrund.

Durch das Verbinden und Trennen von Audiopin 1 ist es möglich, ein nicht zu verwendendes Format zu erreichen. In diesem Fall gibt die [**IMediaFilter::P ause-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) des Filters VFW \_ E NOT CONNECTED \_ \_ zurück. Diese Einschränkung verhindert eine Situation, in der der erste Audioblock über keine Audiodaten verfügt, der zweite Audioblock jedoch über Audiodaten verfügt. Der zweite Block sollte nur Audiodaten haben, wenn der erste Block auch Audio enthält.

Der DV Muxer lässt keine Audioeingaben mit unterschiedlichen Samplingraten zu. Graph-Building-Methoden wie [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) fügen jedoch in der Regel den [ACM-Wrapperfilter](acm-wrapper-filter.md) hinzu, der den zweiten Audiostream so konvertiert, dass er mit der Samplingrate des ersten Streams übereinstimmen kann.

Wenn die Audioeingabe 48 kHz oder 32 kHz beträgt, wird die Audioausgabe gesperrt. (Es ist nicht möglich, Audio mit 44,1 kHz zu sperren.)

Wenn keine Audiopins verbunden sind, enthält die Ausgabe die Audiodaten aus den eingehenden DV-Frames. Dies können Stille oder gültige Audiodaten sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



