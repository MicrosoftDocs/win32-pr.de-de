---
description: DV-Muxer-Filter
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV-Muxer-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747400"
---
# <a name="dv-muxer-filter"></a>DV-Muxer-Filter

Dieser Filter kombiniert einen –-codierten Videostream mit einem oder zwei Audiodatenströmen, um einen verschachtelten DV-Stream zu liefern. Um den Stream in eine AVI-Datei zu schreiben, verbinden Sie diesen Filter mit dem [AVI MUX](avi-mux-filter.md) -Filter, und verbinden Sie die *AVI-MUX* mit dem [dateiwriter](file-writer-filter.md) -Filter. Weitere Informationen finden Sie unter [digitales Video in DirectShow](digital-video-in-directshow.md).



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Eingabe-PIN-Medientypen                    | **Video**: MediaType \_ Video, mediasubtype \_ DVSD, Format \_ videoinfo **-Audiodatei**: MediaType \_ -Audiodatei, mediasubtype \_ PCM, Format \_ WaveFormatEx |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Ausgabe-PIN-Medientypen                   | MediaType \_ interleaved, mediasubtype \_ DVSD, Format \_ dvinfo                                                                             |
| PIN-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| CLSID Filtern                             | CLSID- \_ dvmux                                                                                                                           |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                       |
| Ausführbare Datei                               | qdv.dll                                                                                                                                |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                                                        |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Der DV-Muxer kann zwei audioeingabepins erstellen. Die in der folgenden Tabelle gezeigten Audioformate werden unterstützt.



Audiopin 1

Audiopin 2

Ausgabeformat

Stichproben Rate (kHz)

Bits/Beispiel

Channels

Samplingrate

Bits/Beispiel

Channels

32

16

Mono

Nicht verbundenen

SD 2-Kanal

32

16

Stereo

Nicht verbundenen

SD 4-Kanal

44,1 oder 48

16

Stereo oder Mono

Nicht verbundenen

SD 2-Kanal

Nicht verbundenen

32

16

Stereo oder Mono

Unzulässig

Nicht verbundenen

44,1 oder 48

16

Mono

Unzulässig

Nicht verbundenen

44,1 oder 48

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

44,1

16

Mono

44,1

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

\* Wenn mindestens eine Eingabe-PIN Stereo ist.



 

Für diese Tabelle wird die audiopin 1 als erste Eingabe-PIN definiert, die mit einer Audioquelle verbunden ist, und audiopin 2 wird als zweite Eingabe-PIN definiert, die mit einer Audioquelle verbunden ist. Sobald eine audiopin verbunden ist, bleibt dieses Nummerierungschema wirksam, es sei denn, beide audiopins werden getrennt. Wenn Sie z. b. beide audiopins verbinden und dann die audiopin 1 trennen, wird die verbleibende Pin weiterhin als Pin 2 angesehen.

Audioinformationen für Pin 1 werden im ersten Audioblock der DV-Frames (CH1) aufgezeichnet, und für Pin 2 bereitgestellte Audiodaten werden im zweiten Audioblock (CH2) aufgezeichnet. Ausnahme: Wenn der Filter eine einzelne Stereo Eingabe bei 44,1 kHz oder 48 kHz hat, wird der linke Audiokanal im ersten Audioblock aufgezeichnet, und der Rechte Audiokanal wird im zweiten Audioblock aufgezeichnet.

Für SD 4-Channel-Ausgabe: Wenn die Eingabe Stereo ist, wird der linke Titel in CHa oder CHC aufgezeichnet, und der richtige Titel wird in CHB oder CHD aufgezeichnet. Wenn die Eingabe Mono ist, wird die Audiodatei in CHa oder CHC aufgezeichnet, und CHB und CHD sind stumm.

Wenn Sie die audiopin 1 verbinden und trennen, kann ein unzulässiges Format erreicht werden. In diesem Fall gibt die [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) -Methode des Filters \_ \_ keine Verbindung mit VFW E zurück \_ . Diese Einschränkung verhindert eine Situation, in der der erste Audioblock keine Audiodaten aufweist, aber der zweite Audioblock über Audiodaten verfügt. Der zweite Block sollte nur Audiodaten enthalten, wenn der erste Block auch Audiodaten enthält.

Der DV-Muxer lässt keine Audioeingaben mit unterschiedlichen Stichproben Raten zu. Allerdings fügen Diagramm Erstellungs Methoden, wie z. b. [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) , in der Regel den [ACM-Wrapper](acm-wrapper-filter.md) Filter hinzu, der den zweiten Audiostream entsprechend der Stichprobenrate des ersten Streams konvertiert.

Wenn die Audioeingabe 48 kHz oder 32 kHz ist, wird die Audioausgabe gesperrt. (Es ist nicht möglich, 44,1-kHz-Audiodaten zu sperren.)

Wenn keine audiopins verbunden sind, enthält die Ausgabe die Audiodaten der eingehenden DV-Frames. Dies kann ein schweige Wert oder gültige Audiodaten sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



