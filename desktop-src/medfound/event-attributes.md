---
description: Ereignisattribute
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Ereignis Attribute (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524531"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Ereignis Attribute (Microsoft Media Foundation)

Die folgenden Attribute gelten für Ereignisse.



| Attribut                                                                                                        | BESCHREIBUNG                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF- \_ Ereignis wird \_ \_ dünner**](mf-event-do-thinning-attribute.md)                                                | Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt an, ob die Quelle auch eine Verdünnung anfordert.                |
| [**MF- \_ Ereignis \_ Ausgabe \_ Knoten**](mf-event-output-node-attribute.md)                                                | Identifiziert den topologieknoten für eine streamsenke.                                                                       |
| [**Zeit Offset der MF- \_ Ereignis \_ Präsentation \_ \_**](mf-event-presentation-time-offset-attribute.md)                     | Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.                                              |
| [**\_ \_ scrubsample-Zeit für MF-Ereignis \_**](mf-event-scrubsample-time-attribute.md)                                      | Präsentationszeit für ein Beispiel, das beim Scrubbing gerendert wurde.                                                     |
| [**MF- \_ Ereignis \_ sessioncaps**](mf-event-sessioncaps-attribute.md)                                                 | Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.                  |
| [**\_Delta-Ereignis \_ sessioncaps- \_ Delta**](mf-event-sessioncaps-delta-attribute.md)                                    | Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden. |
| [**Beginn der MF- \_ Ereignis \_ Quelle \_ \_**](mf-event-source-actual-start-attribute.md)                               | Enthält die Startzeit, zu der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.                                       |
| [**Eigenschaften der MF- \_ Ereignis \_ Quelle \_**](mf-event-source-characteristics-attribute.md)                          | Gibt die aktuellen Merkmale der Medienquelle an.                                                            |
| [**Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ alt**](mf-event-source-characteristics-old-attribute.md)                 | Gibt die früheren Merkmale der Medienquelle an.                                                           |
| [**der MF- \_ Ereignis \_ Quelle wurde \_ \_ gestartet.**](mf-event-source-fake-start-attribute.md)                                   | Gibt an, ob die aktuelle Segment Topologie leer ist.                                                              |
| [**der MF- \_ Ereignis \_ Quelle \_ ProjectStart**](mf-event-source-projectstart-attribute.md)                                | Gibt die Startzeit für eine Segment Topologie an.                                                                      |
| [**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**](mf-event-source-topology-canceled-attribute.md)                     | Gibt an, ob die Sequencer-Quelle eine Topologie abgebrochen hat.                                                           |
| [**\_ \_ Start \_ Präsentations \_ Zeit für MF-Ereignis**](mf-event-start-presentation-time-attribute.md)                       | Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.               |
| [**\_ \_ \_ \_ Zeitpunkt der Ausgabe Präsentation des MF-Ereignisses \_ bei der \_ Ausgabe**](mf-event-start-presentation-time-at-output-attribute.md) | Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.                      |
| [**Status der MF- \_ Ereignis \_ Topologie \_**](mf-event-topology-status-attribute.md)                                        | Gibt den Status einer Topologie während der Wiedergabe an.                                                                   |
| [**MF- \_ Sitzung \_ ca. \_ Ereignis \_ vorkommen \_ Zeit**](mf-session-approx-event-occurrence-time-attribute.md)        | Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



