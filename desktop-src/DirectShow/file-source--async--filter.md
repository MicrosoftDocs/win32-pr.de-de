---
description: Filter für Datei Quelle (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filter für Datei Quelle (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481646"
---
# <a name="file-source-async-filter"></a>Filter für Datei Quelle (Async)

Der asynchrone Datei Quellen Filter öffnet und liest lokale Dateien vieler verschiedener Datenformate und übergibt die Daten an einen Parserfilter.

Um Mediendateien über HTTP aus dem Internet herunterzuladen, verwenden Sie den Filter für die [Datei Quelle (URL)](file-source--url--filter.md) . Verwenden Sie zum Lesen von ASF-Dateien den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter.



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Eingabe-PIN-Medientypen                    | Nicht verfügbar                                                                                                                       |
| PIN-Eingabeschnittstellen                     | Nicht verfügbar                                                                                                                       |
| Ausgabe-PIN-Medientypen                   | **MediaType \_ Stream**. Der Untertyp hängt vom Medienformat ab. (**Mediasubtype \_ null** , wenn der Filter das Format nicht erkennt). |
| PIN-Schnittstellen                    | [**Iamasynkreadertimestampscaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID Filtern                             | **CLSID- \_ asynshader**                                                                                                               |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                           |
| [Verdienst](merit.md)                       | **nicht \_ wahrscheinlich**                                                                                                                  |
| [Filter Kategorie](filter-categories.md) | **CLSID \_ legacyamfiltercategory**                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



