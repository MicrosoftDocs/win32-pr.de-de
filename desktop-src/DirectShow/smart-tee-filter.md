---
description: Smart Tee-Filter
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart Tee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482299"
---
# <a name="smart-tee-filter"></a>Smart Tee-Filter

Der Smart Tee-Filter wird in Video Erfassungs Diagrammen verwendet, um den Videostream in einen Vorschau Datenstrom und einen Aufzeichnungsdaten Strom aufzuteilen. Dies erfolgt ohne zusätzliches Kopieren von Daten. Die Ausgabe Pins unterstützen alle Medientypen, die von der Downstream-Verbindung unterstützt werden.

Der Smart Tee-Filter ist nützlich, wenn ein Video Erfassungs Filter keine separaten Pins für Erfassung und Vorschau bereitstellt. Der Smart Tee-Filter liefert nur die Vorschau Daten, wenn dies die Leistungs Erfassung nicht beeinträchtigt. Außerdem werden die Zeitstempel aus dem Vorschau Datenstrom entfernt. Der Erfassungs Diagramm-Generator fügt bei Bedarf automatisch den intelligenten Tee-Filter ein. Weitere Informationen finden Sie unter [Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md).

Die folgende Abbildung zeigt ein typisches Erfassungs Diagramm, das den intelligenten Tee-Filter verwendet.

![Verwenden des Smart Tee-Filters](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Eingabe-PIN-Medientypen                    | MediaType- \_ Video, mediasubtype \_ null                                                                           |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Ausgabe-PIN-Medientypen                   | MediaType- \_ Video, mediasubtype \_ null                                                                           |
| PIN-Schnittstellen                    | [**Iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ smarttee                                                                                                |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                              |
| Ausführbare Datei                               | qcap.dll                                                                                                       |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                            |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Die Erfassungs-PIN ist die Ausgabe-PIN 0, und die Vorschau-PIN lautet Ausgabe-PIN 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



