---
description: Ereignisattribute
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Ereignisattribute (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600510"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Ereignisattribute (Microsoft Media Foundation)

Die folgenden Attribute gelten für Ereignisse.



| attribute                                                                                                        | Beschreibung                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ DO \_ THINNING**](mf-event-do-thinning-attribute.md)                                                | Wenn eine Medienquelle eine neue Wiedergaberate anfordert, gibt an, ob die Quelle ebenfalls eine Ausschmalung anfordert.                |
| [**\_ \_ MF-EREIGNISAUSGABEKNOTEN \_**](mf-event-output-node-attribute.md)                                                | Identifiziert den Topologieknoten für eine Streamsenke.                                                                       |
| [**\_ \_ \_ MF-EREIGNISPRÄSENTATIONSZEITOFFSET \_**](mf-event-presentation-time-offset-attribute.md)                     | Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.                                              |
| [**MF \_ EVENT \_ SCRUBSAMPLE \_ TIME**](mf-event-scrubsample-time-attribute.md)                                      | Präsentationszeit für ein Beispiel, das während der Bereinigung gerendert wurde.                                                     |
| [**MF \_ EVENT \_ SESSIONCAPS**](mf-event-sessioncaps-attribute.md)                                                 | Enthält Flags, die die Funktionen der Mediensitzung basierend auf der aktuellen Präsentation definieren.                  |
| [**MF \_ EVENT \_ SESSIONCAPS \_ DELTA**](mf-event-sessioncaps-delta-attribute.md)                                    | Enthält Flags, die angeben, welche Funktionen sich in der Mediensitzung basierend auf der aktuellen Präsentation geändert haben. |
| [**\_ \_ MF-EREIGNISQUELLE \_ TATSÄCHLICHER \_ START**](mf-event-source-actual-start-attribute.md)                               | Enthält die Startzeit, zu der eine Medienquelle von ihrer aktuellen Position aus neu gestartet wird.                                       |
| [**MERKMALE \_ DER MF-EREIGNISQUELLE \_ \_**](mf-event-source-characteristics-attribute.md)                          | Gibt die aktuellen Merkmale der Medienquelle an.                                                            |
| [**\_ \_ MF-EREIGNISQUELLENMERKMALE \_ \_ ALT**](mf-event-source-characteristics-old-attribute.md)                 | Gibt die vorherigen Merkmale der Medienquelle an.                                                           |
| [**MF \_ EVENT \_ SOURCE \_ FAKE \_ START**](mf-event-source-fake-start-attribute.md)                                   | Gibt an, ob die aktuelle Segmenttopologie leer ist.                                                              |
| [**\_MF-EREIGNISQUELLE \_ \_ PROJEKTSTART**](mf-event-source-projectstart-attribute.md)                                | Gibt die Startzeit für eine Segmenttopologie an.                                                                      |
| [**\_ \_ MF-EREIGNISQUELLENTOPOLOGIE \_ \_ ABGEBROCHEN**](mf-event-source-topology-canceled-attribute.md)                     | Gibt an, ob die Sequencerquelle eine Topologie abgebrochen hat.                                                           |
| [**\_ \_ \_ MF-EREIGNISSTARTPRÄSENTATIONSZEIT \_**](mf-event-start-presentation-time-attribute.md)                       | Die Startzeit für die Präsentation in Einheiten von 100 Nanosekunden, gemessen an der Präsentationsuhr.               |
| [**START \_ \_ DER PRÄSENTATIONSZEIT DES MF-EREIGNISSES \_ BEI \_ DER \_ \_ AUSGABE**](mf-event-start-presentation-time-at-output-attribute.md) | Die Präsentationszeit, zu der die Mediensenken das erste Beispiel der neuen Topologie rendern.                      |
| [**STATUS \_ DER MF-EREIGNISTOPOLOGIE \_ \_**](mf-event-topology-status-attribute.md)                                        | Gibt den Status einer Topologie während der Wiedergabe an.                                                                   |
| [**MF \_ SESSION \_ APPROX \_ EVENT \_ OCCURRENCE \_ TIME**](mf-session-approx-event-occurrence-time-attribute.md)        | Die ungefähre Zeit, zu der die Mediensitzung ein Ereignis ausgelöst hat.                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**WFMEDIAEVENT**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



