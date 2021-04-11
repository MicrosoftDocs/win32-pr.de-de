---
description: VGA-Filter mit 16 Farben ditherer
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA-Filter mit 16 Farben ditherer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042555"
---
# <a name="vga-16-color-ditherer-filter"></a>VGA-Filter mit 16 Farben ditherer

Der Modus für die VGA-Auflösung von 16 Farben wird von einem RGB-Farbtyp in eine 4-Bit-Farbanzeige konvertiert, sodass AVI-und MPEG-Videostreams auf älteren 16-farbigen Monitoren angezeigt werden können. Dieser Filter wird im Diagramm zwischen einem Debug-Filter und einem Videorendererfilter eingefügt.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabe-PIN-Medientypen                    | MediaType \_ Video, mediasubtype \_ RGB8                                                                                                               |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabe-PIN-Medientypen                   | MediaType \_ Video, mediasubtype \_ RGB4                                                                                                               |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ Dither                                                                                                                                      |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                  |
| Ausführbare Datei                               | quartz.dll                                                                                                                                         |
| [Verdienst](merit.md)                       | nicht \_ wahrscheinlich                                                                                                                                    |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



