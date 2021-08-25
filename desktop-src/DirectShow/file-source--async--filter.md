---
description: Dateiquellenfilter (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Dateiquellenfilter (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9261cc65774fc6116a902a02ef193a205ca83ce4232a30534e7b38c040c01971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000741"
---
# <a name="file-source-async-filter"></a>Dateiquellenfilter (Async)

Der Filter Asynchrone Dateiquelle öffnet lokale Dateien von vielen verschiedenen Datenformaten und liest sie und übergibt die Daten an einen Parserfilter.

Verwenden Sie zum Herunterladen von Mediendateien aus dem Web über HTTP den Filter [Dateiquelle (URL).](file-source--url--filter.md) Verwenden Sie zum Lesen von ASF-Dateien den [WM ASF-Readerfilter.](wm-asf-reader-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Eingabepinmedientypen                    | Nicht zutreffend                                                                                                                       |
| Eingabe-Pin-Schnittstellen                     | Nicht zutreffend                                                                                                                       |
| Medientypen des Ausgabepins                   | **MEDIATYPE \_ Streamen** Sie . Der Untertyp hängt vom Medienformat ab. (**MEDIASUBTYPE \_ NULL,** wenn der Filter das Format nicht erkennt.) |
| Ausgabe-Pin-Schnittstellen                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| Filtern von CLSID                             | **CLSID \_ AsyncReader**                                                                                                               |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                           |
| [Verdienst](merit.md)                       | **\_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT**                                                                                                                  |
| [Filterkategorie](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



