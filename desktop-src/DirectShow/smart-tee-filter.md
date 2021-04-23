---
description: Smart Tee-Filter
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart Tee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909298"
---
# <a name="smart-tee-filter"></a>Smart Tee-Filter

Der Smart Tee-Filter wird in Videoaufnahmediagrammen verwendet, um den Videostream in einen Vorschaustream und einen Erfassungsstream aufzuteilen. Dies erfolgt ohne zusätzliches Kopieren von Daten. Die Ausgabepins unterstützen alle Medientypen, die für die Downstreamverbindung unterstützt werden.

Der Smart Tee-Filter ist nützlich, wenn ein Videoaufnahmefilter keine separaten Pins für die Erfassung und Vorschau bereitstellt. Der Smart Tee-Filter liefert nur Dann Vorschaudaten, wenn dies die Erfassungsleistung nicht beeinträchtigt. Außerdem werden die Zeitstempel aus dem Vorschaustream entfernt. Der Generator für Erfassungsgraphen fügt bei Bedarf automatisch den Smart Tee-Filter ein. Weitere Informationen finden Sie unter [Kombinieren von Video capture und Preview](combining-video-capture-and-preview.md).

Die folgende Abbildung zeigt ein typisches Erfassungsdiagramm, das den Smart Tee-Filter verwendet.

![Verwenden des Smart Tee-Filters](images/smarttee.png)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                           |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                           |
| Ausgabe-PIN-Schnittstellen                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ SmartTee                                                                                                |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite.                                                                                              |
| Ausführbare Datei                               | qcap.dll                                                                                                       |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                            |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Der Aufnahmepin ist der Ausgabepin 0, und der Vorschaupin ist der Ausgabepin 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



