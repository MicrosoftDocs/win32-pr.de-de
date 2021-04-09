---
description: Informationen zum WM-ASF-Reader-Filter
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informationen zum WM-ASF-Reader-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860423"
---
# <a name="about-the-wm-asf-reader-filter"></a>Informationen zum WM-ASF-Reader-Filter

Die Wiedergabe von ASF-Dateien wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter behandelt. Wenn der WM-ASF-Reader eine Datei liest, erstellt er automatisch eine Ausgabe-PIN für jeden Stream, einschließlich Webstreams, Skript befehlsstreams und beliebiger anderer Typen von beliebigem Stream. Im Fall von Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt. Um eine ASF-Datei mit dem WM-ASF-Reader-Filter wiederzugeben, müssen Sie [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) oder [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)aufrufen.

Der WM-ASF-Reader unterstützt die Schnittstelle DirectShow [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , mit der Anwendungen eine temporale Suche innerhalb der Datei durchführen können. Die Wiedergabe mit einer anderen Geschwindigkeit als 1,0 (wie in [**imediaseeking::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)* angegeben) wird jedoch nicht unterstützt.

Der WM-ASF-Lesefilter macht auch mehrere Windows Media-Format-SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben. Diese Schnittstellen sind in der Dokumentation zum Windows Media-Format SDK dokumentiert.



| Schnittstelle                                             | Verfügbar gemacht                                 | Kommentare                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Über **IServiceProvider** für den Filter. | Wird für Anwendungen bereitgestellt, die durch Digital Rights Management (DRM) geschützte Inhalte wiedergeben müssen.                             |
| [**Iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** für den Filter.           | Bereitgestellt, damit Anwendungen Datei-und Inhalts Attribute sowie Marker-und Skriptinformationen sowie Metadaten lesen können.     |
| [**Iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** für den Filter.           | Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des WM-Reader-Objekts zugreifen können.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** für den Filter.           | Teilweise für den Filter implementiert, sodass Anwendungen auf die Informationsmethoden des Format-SDK-Reader-Objekts zugreifen können. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



