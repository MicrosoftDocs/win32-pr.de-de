---
description: Navigationsleiste des analogen Videos
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Navigationsleiste des analogen Videos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957889"
---
# <a name="analog-video-crossbar-filter"></a>Navigationsleiste des analogen Videos

Der Symbolleisten Filter für die analoge Video Darstellung stellt eine Video quer Leiste auf einem Video Erfassungsgerät dar, das die Windows-Treibermodell (WDM) unterstützt.

Dieser Filter ist ein Wrapper Filter für crossbars auf WDM-Streaminggeräten. Der Anzeige Name des Filters wird vom Gerät übernommen. Jeder Ausgabepin stellt einen Hardware Pfad für das analoge Baseband-Video dar. Einer der Eingabe Pins stammt von einem TV-Tuner (der [TV-Tuner-Filter](tv-tuner-filter.md)). Andere Eingabe-Pins unterstützen Video-oder Audiostreams. Der Filter unterstützt alle Medien Untertypen und Formate, die von den downstreamverbindungen unterstützt werden.

Dieser Filter kann nicht direkt mit cokreatanstance erstellt werden. Die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle fügt diesen Filter nach Bedarf automatisch dem Diagramm hinzu.

Weitere Informationen zu Wrapper Filtern und WDM-Streaminggeräten finden Sie unter [wie Hardware Geräte am Filter Diagramm teilnehmen](how-hardware-devices-participate-in-the-filter-graph.md).



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamcrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Eingabe-PIN-Medientypen                    | MediaType \_ Analog gaudiodatei, MediaType \_ Analog gvideo                                                 |
| PIN-Eingabeschnittstellen                     | [**"Ikspropertyset"**](ikspropertyset.md)                                                       |
| Ausgabe-PIN-Medientypen                   | MediaType \_ Analog gaudiodatei, MediaType \_ Analog gvideo                                                 |
| PIN-Schnittstellen                    | [**"Ikspropertyset"**](ikspropertyset.md)                                                       |
| CLSID Filtern                             | Nicht verfügbar                                                                                 |
| CLSID der Eigenschaften Seite                      | CLSID \_ crossbarfilterpropertypage                                                              |
| Ausführbare Datei                               | ksxbar.ax                                                                                      |
| [Verdienst](merit.md)                       | Treiber abhängig.                                                                              |
| [Filter Kategorie](filter-categories.md) | AM- \_ kscategory- \_ Querstrich                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Arbeiten mit quer leisten](working-with-crossbars.md)
</dt> </dl>

 

 



