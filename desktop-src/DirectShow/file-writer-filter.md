---
description: Dateiwriter-Filter
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Dateiwriter-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213971"
---
# <a name="file-writer-filter"></a>Dateiwriter-Filter

Der dateiwriter-Filter kann verwendet werden, um Dateien unabhängig vom Format auf die Festplatte zu schreiben. Der Filter schreibt einfach auf die Festplatte, die er in der Eingabe-PIN empfängt, sodass er mit einem Multiplexer verbunden werden muss, der die Datei ordnungsgemäß formatieren kann. Sie können eine neue Ausgabedatei mit dem dateiwriter erstellen oder eine vorhandene Datei angeben. Wenn die Datei bereits vorhanden ist, wird Sie vollständig mit den neuen Daten überschrieben.

Der dateiwriter-Filter verwendet die Zeitstempel des Eingabedaten Stroms als Dateioffsets und bietet zufälligen Zugriff auf die Datei. Es unterstützt **IStream** , um das Lesen und Schreiben der Datei Kopfzeile nach dem Beenden des Diagramms zuzulassen. Um die Leistung zu verbessern, unterstützt es auch nicht gepufferte Schreibvorgänge und verarbeitet die entsprechende Puffer Aushandlung.

> [!Note]  
> Verwenden Sie zum Schreiben von ASF-Dateien den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter.

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamfilterfehlflags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream** |
| Eingabe-PIN-Medientypen                    | MediaType \_ Stream, mediasubtype \_ null                                                                                                                                                              |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Ausgabe-PIN-Medientypen                   | Nicht verfügbar                                                                                                                                                                                     |
| PIN-Schnittstellen                    | Nicht verfügbar                                                                                                                                                                                     |
| CLSID Filtern                             | CLSID- \_ FileWriter                                                                                                                                                                                  |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



