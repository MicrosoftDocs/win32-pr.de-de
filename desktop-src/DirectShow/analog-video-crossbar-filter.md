---
description: Analog Video Crossbar Filter
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Analog Video Crossbar Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909598"
---
# <a name="analog-video-crossbar-filter"></a>Analog Video Crossbar Filter

Der Analog Video Crossbar-Filter stellt eine Video-Querleiste auf einem Videoaufnahmegerät dar, das die Windows-Treibermodell (WDM) unterstützt.

Dieser Filter ist ein Wrapperfilter für Querleisten auf WDM-Streaminggeräten. Der Angezeigte Name des Filters wird vom Gerät übernommen. Jeder Ausgabepin stellt einen Hardwarepfad für analoges Basebandvideo dar. Einer der Eingabepins stammt von einem TV-Tuner [(tv tuner Filter).](tv-tuner-filter.md) Andere Eingabepins unterstützen Video- oder Audiostreams. Der Filter unterstützt alle Medienuntertypen und Formate, die für die Downstreamverbindungen unterstützt werden.

Sie können diesen Filter nicht direkt mit CoCreateInstance erstellen. Die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fügt diesen Filter bei Bedarf automatisch dem Diagramm hinzu.

Weitere Informationen zu Wrapperfiltern und WDM-Streaminggeräten finden Sie unter [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).



| Bezeichnung | Wert |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Eingabepin-Medientypen                    | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Eingabepinschnittstellen                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Ausgabepin-Medientypen                   | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Ausgabe-Pin-Schnittstellen                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Filtern von CLSID                             | Nicht zutreffend                                                                                 |
| CLSID der Eigenschaftenseite                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| Ausführbare Datei                               | ksxbar.ax                                                                                      |
| [Verdienst](merit.md)                       | Treiberabhängig.                                                                              |
| [Filterkategorie](filter-categories.md) | AM \_ KSCATEGORY \_ CROSSBAR                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Arbeiten mit Querleisten](working-with-crossbars.md)
</dt> </dl>

 

 



