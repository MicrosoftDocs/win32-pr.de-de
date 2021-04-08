---
description: MIDI-Parser-Filter
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: MIDI-Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957733"
---
# <a name="midi-parser-filter"></a>MIDI-Parser-Filter

Der MIDI-Parser-Filter liest die in gefundenen Daten in. Mid und. RMI-Dateien. Der Filter akzeptiert einen Stream aus den Quell Filtern der asynchronen [Datei Quelle](file-source--async--filter.md) oder der [URL-Datei](file-source--url--filter.md) und gibt die für die Wiedergabe verwendeten MIDI-Beispiele an den [**MIDI-Renderer**](midi-renderer-filter.md)



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Eingabe-PIN-Medientypen                    | MediaType \_ Stream, mediasubtype \_ MIDI                                                                    |
| PIN-Eingabeschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Ausgabe-PIN-Medientypen                   | MediaType \_ MIDI, mediasubtype \_ null                                                                      |
| PIN-Schnittstellen                    | [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID Filtern                             | CLSID- \_ midiparser                                                                                        |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                         |
| Ausführbare Datei                               | quartz.dll                                                                                               |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                          |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [**MIDI-Renderer**](midi-renderer-filter.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



