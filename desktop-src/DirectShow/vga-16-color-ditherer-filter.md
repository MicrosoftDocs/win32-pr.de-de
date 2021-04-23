---
description: VGA 16 Color Ditherer Filter
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA 16 Color Ditherer Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908678"
---
# <a name="vga-16-color-ditherer-filter"></a>VGA 16 Color Ditherer Filter

Der VGA 16 Color Ditherer-Filter konvertiert von einem RGB-Farbtyp in eine 4-Bit-Farbanzeige, sodass AVI- und MPEG-Videostreams auf älteren Monitoren mit 16 Farben angezeigt werden können. Dieser Filter wird in das Diagramm zwischen einem Dekomprimiererfilter und einem Videorendererfilter eingefügt.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ Dither                                                                                                                                      |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                                                                  |
| Ausführbare Datei                               | quartz.dll                                                                                                                                         |
| [Verdienst](merit.md)                       | WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH                                                                                                                                    |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



