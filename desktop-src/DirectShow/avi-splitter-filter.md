---
description: AVI-Splitterfilter
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI-Splitterfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909658"
---
# <a name="avi-splitter-filter"></a>AVI-Splitterfilter

Der AVI-Splitterfilter wird für die Wiedergabe von AVI-Dateien verwendet. Sie akzeptiert Daten im AVI-Format und teilt sie zur weiteren Verarbeitung und/oder zum Rendern in die konstituierenden Datenströme auf.



| Bezeichnung | Wert |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Eingabepin-Medientypen                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi                                                                                                                                |
| Eingabepinschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Ausgabepin-Medientypen                   | In der Regel **MEDIATYPE \_ Video** oder **MEDIATYPE \_ Audio**. Der genaue Typ hängt vom Inhalt der Datei ab, davon, ob die Datei komprimiert ist und welcher Codec verwendet wurde. |
| Ausgabe-PIN-Schnittstellen                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| Filtern der CLSID                             | CLSID \_ AviSplitter                                                                                                                                                  |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                          |
| [Verdienst](merit.md)                       | NORMALER WERT \_                                                                                                                                                       |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter ist in der Regel mit dem Filter [Async File Source (Asynchrone Dateiquelle)](file-source--async--filter.md) auf dem Eingabepin verbunden. Er kann eine Verbindung mit jedem Filter herstellen, dessen Ausgabepin [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt, und bietet den richtigen Medientyp für den Eingabepin des AVI-Splitterfilters.

Die Ausgabepins auf dem AVI-Splitter unterstützen die IPropertyBag::Read-Methode zum Lesen von Eigenschaften aus einzelnen Streams. Derzeit ist die folgende Eigenschaft definiert.



| Eigenschaft | BESCHREIBUNG                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Gibt den Namen des Streams aus dem `'strn'` Block in der AVI-Datei zurück. Wenn dieser Block nicht vorhanden ist, gibt die Read-Methode E \_ INVALIDARG zurück. |



 

Die IPropertyBag::Write-Methode gibt E \_ FAIL zurück. Der [AVI Mux-Filter](avi-mux-filter.md) unterstützt IPropertyBag::Write zum Speichern von Streameigenschaften in einer AVI-Datei.

Der AVI-Splitter lässt nicht zu, dass Downstreamfilter einen eigenen Allocator verwenden.

Die Verschachtelungsdauer in der Datei bestimmt, wie viel Arbeitsspeicher der AVI-Splitter für die Verarbeitung zuweist. Eine Datei, die in Blöcken von einer Sekunde überlappend ist, benötigt viel mehr Arbeitsspeicher für die Verarbeitung als eine Datei, deren Verschachtelungsdauer auf ein oder zwei Frames festgelegt ist. Auf modernen Computern ist dies in der Regel kein Problem, es sei denn, Sie führen mehrere Instanzen des AVI-Splitters gleichzeitig aus.

### <a name="seeking"></a>Suchen

Wenn die Datei einen Videostream enthält, unterstützt der AVI-Splitter suchweise nach Framenummer. Um die framebasierte Suche zu aktivieren, rufen Sie [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filtergraph-Manager](filter-graph-manager.md) mit dem Wert **TIME FORMAT \_ \_ FRAME** auf.

Wenn die Datei einen Audiodatenstrom enthält, unterstützt der AVI-Splitter Such- nach Beispielnummer. Um die beispielbasierte Suche zu aktivieren, rufen [**Sie SetTimeFormat im**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) Filterdiagramm-Manager mit dem Wert **TIME FORMAT SAMPLE \_ \_ auf.**

In beiden Fällen muss der Ausgabepin für diesen Stream mit einem Rendererfilter verbunden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



