---
description: Smart Tee-Filter
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart Tee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a8e829d78658b867d3884240250c10d10a65c7cd309f109fe29b023c726518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964995"
---
# <a name="smart-tee-filter"></a>Smart Tee-Filter

Der Smart Tee-Filter wird in Videoaufzeichnungsdiagrammen verwendet, um den Videostream in einen Vorschaustream und einen Erfassungsstream aufzuteilen. Dies erfolgt ohne zusätzliches Kopieren von Daten. Die Ausgabepins unterstützen alle Medientypen, die für die Downstreamverbindung unterstützt werden.

Der Smart Tee-Filter ist nützlich, wenn ein Videoaufnahmefilter keine separaten Pins für die Erfassung und Vorschau bereitstellt. Der Smart Tee-Filter liefert nur Dann Vorschaudaten, wenn dies die Erfassungsleistung nicht beeinträchtigt. Außerdem werden die Zeitstempel aus dem Vorschaustream entfernt. Der Generator für Erfassungsgraphen fügt bei Bedarf automatisch den Smart Tee-Filter ein. Weitere Informationen finden Sie unter [Kombinieren von Video capture und Preview](combining-video-capture-and-preview.md).

Die folgende Abbildung zeigt ein typisches Erfassungsdiagramm, das den Smart Tee-Filter verwendet.

![Verwenden des Smart Tee-Filters](images/smarttee.png)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Eingabepinmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                           |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL                                                                           |
| Ausgabe-Pin-Schnittstellen                    | [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ SmartTee                                                                                                |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                              |
| Ausführbare Datei                               | qcap.dll                                                                                                       |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                            |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Hinweise

Der Erfassungspin ist der Ausgabepin 0, und der Vorschaupin ist Ausgabepin 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



