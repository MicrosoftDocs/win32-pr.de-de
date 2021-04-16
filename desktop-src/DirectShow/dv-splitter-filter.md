---
description: DV-Splitter Filter
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: DV-Splitter Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ada4f18a107f8e1b07571f3907aed5ddf50f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520555"
---
# <a name="dv-splitter-filter"></a>DV-Splitter Filter

Dieser Filter teilt einen überlappenden digitalen Videodaten Strom (DV) in seine Komponenten Video-und Audiodatenströme auf.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **idvsplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Eingabe-PIN-Medientypen                    | MediaType \_ interleaved, mediasubtype \_ DVSD, Format \_ dvinfo                                                                                         |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabe-PIN-Medientypen                   | **Video**: MediaType- \_ Video, Format \_ dvinfo<br/> **Audiodatei**: MediaType \_ -Audiodatei, mediasubtype \_ PCM, Format \_ WaveFormatEx<br/>             |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ dvsplitter                                                                                                                                  |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                  |
| Ausführbare Datei                               | qdv.dll                                                                                                                                            |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                      |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

DV-Frames enthalten Audiodateien und Videos im gleichen Frame. Der DV-Splitter Filter extrahiert die Audiodaten und übermittelt sie als einen oder zwei Audiostreams aus den audioausgabepins. Der ursprüngliche DV-Frame wird von der Videoausgabe-Pin als Videoframe übermittelt. Der Medientyp im Videoframe wird von MediaType \_ in MediaType \_ Video geändert, aber andernfalls werden die Daten nicht geändert. Der Medientyp wird geändert, um zu signalisieren, dass die Audiodaten im Frame ignoriert werden sollten. Der DV-Splitter legt keine Medien Zeit in seinen Ausgabe Beispielen fest. Wenn Sie einen downstreamfilter schreiben, der die Medien Zeiten erfordert, können Sie die Uhrzeiten von der Frame Anzahl ableiten.

Die Schnittstellen [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) werden jeweils nur von einer Ausgabe-PIN verfügbar gemacht.

Der DV-Splitter Filter kann dynamische Formatänderungen im Audiostream akzeptieren. Wenn der [AVI MUX](avi-mux-filter.md) -Filter jedoch Downstream ist, wird die Formatänderung abgelehnt. Wenn dies der Fall ist, beendet der DV-Splitter die Erstellung eines Audiostreams. Diese Einschränkung wirkt sich nur auf die Datei Erfassung von Type-2 aus. Bei Type-1-Dateien wird der verschachtelte Stream nicht an erster Stelle aufgeteilt. Für die Vorschau gibt es keinen nachgelagerten AVI MUX-Filter.

Wenn es sich bei der DV-Quelle um eine Live Kamera handelt, gibt es normalerweise keinen Grund, dass das Audioformat geändert werden muss. Das Format kann sich jedoch ändern, wenn Sie von einem VTR-Band übertragen, das mehrere heterogene Quellen enthält.

Jeder DV-Frame enthält zusätzlich zu den Audiodaten und Videodaten Metadaten. Diese Metadaten können von Frame zu Frame geändert werden. Anwendungen können die Metadaten analysieren, indem Sie entweder die Eingabe Beispiele oder die Videoausgabe Beispiele überprüfen. DirectShow bietet jedoch keine direkte Unterstützung für die bidirekmieren von DV-Metadaten. Weitere Informationen finden Sie unter IEC 61834-4.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




