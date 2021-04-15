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
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="194a7-103">Ereignis Attribute (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="194a7-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="194a7-104">Die folgenden Attribute gelten für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="194a7-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="194a7-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="194a7-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="194a7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="194a7-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="194a7-107">**MF- \_ Ereignis wird \_ \_ dünner**</span><span class="sxs-lookup"><span data-stu-id="194a7-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="194a7-108">Wenn eine Medienquelle eine neue Wiedergabe Rate anfordert, gibt an, ob die Quelle auch eine Verdünnung anfordert.</span><span class="sxs-lookup"><span data-stu-id="194a7-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="194a7-109">**MF- \_ Ereignis \_ Ausgabe \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="194a7-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="194a7-110">Identifiziert den topologieknoten für eine streamsenke.</span><span class="sxs-lookup"><span data-stu-id="194a7-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="194a7-111">**Zeit Offset der MF- \_ Ereignis \_ Präsentation \_ \_**</span><span class="sxs-lookup"><span data-stu-id="194a7-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="194a7-112">Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="194a7-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="194a7-113">**\_ \_ scrubsample-Zeit für MF-Ereignis \_**</span><span class="sxs-lookup"><span data-stu-id="194a7-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="194a7-114">Präsentationszeit für ein Beispiel, das beim Scrubbing gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="194a7-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="194a7-115">**MF- \_ Ereignis \_ sessioncaps**</span><span class="sxs-lookup"><span data-stu-id="194a7-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="194a7-116">Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.</span><span class="sxs-lookup"><span data-stu-id="194a7-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="194a7-117">**\_Delta-Ereignis \_ sessioncaps- \_ Delta**</span><span class="sxs-lookup"><span data-stu-id="194a7-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="194a7-118">Enthält Flags, die angeben, welche Funktionen in der Medien Sitzung basierend auf der aktuellen Präsentation geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="194a7-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="194a7-119">**Beginn der MF- \_ Ereignis \_ Quelle \_ \_**</span><span class="sxs-lookup"><span data-stu-id="194a7-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="194a7-120">Enthält die Startzeit, zu der eine Medienquelle von Ihrer aktuellen Position neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="194a7-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="194a7-121">**Eigenschaften der MF- \_ Ereignis \_ Quelle \_**</span><span class="sxs-lookup"><span data-stu-id="194a7-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="194a7-122">Gibt die aktuellen Merkmale der Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="194a7-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="194a7-123">**Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ alt**</span><span class="sxs-lookup"><span data-stu-id="194a7-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="194a7-124">Gibt die früheren Merkmale der Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="194a7-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="194a7-125">**der MF- \_ Ereignis \_ Quelle wurde \_ \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="194a7-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="194a7-126">Gibt an, ob die aktuelle Segment Topologie leer ist.</span><span class="sxs-lookup"><span data-stu-id="194a7-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="194a7-127">**der MF- \_ Ereignis \_ Quelle \_ ProjectStart**</span><span class="sxs-lookup"><span data-stu-id="194a7-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="194a7-128">Gibt die Startzeit für eine Segment Topologie an.</span><span class="sxs-lookup"><span data-stu-id="194a7-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="194a7-129">**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="194a7-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="194a7-130">Gibt an, ob die Sequencer-Quelle eine Topologie abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="194a7-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="194a7-131">**\_ \_ Start \_ Präsentations \_ Zeit für MF-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="194a7-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="194a7-132">Die Startzeit für die Präsentation in 100-Nanosecond-Einheiten, gemessen an der Präsentations Uhr.</span><span class="sxs-lookup"><span data-stu-id="194a7-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="194a7-133">**\_ \_ \_ \_ Zeitpunkt der Ausgabe Präsentation des MF-Ereignisses \_ bei der \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="194a7-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="194a7-134">Die Präsentationszeit, zu der die Medien senken das erste Beispiel der neuen Topologie Rendering.</span><span class="sxs-lookup"><span data-stu-id="194a7-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="194a7-135">**Status der MF- \_ Ereignis \_ Topologie \_**</span><span class="sxs-lookup"><span data-stu-id="194a7-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="194a7-136">Gibt den Status einer Topologie während der Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="194a7-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="194a7-137">**MF- \_ Sitzung \_ ca. \_ Ereignis \_ vorkommen \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="194a7-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="194a7-138">Der ungefähre Zeitpunkt, zu dem die Medien Sitzung ein Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="194a7-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="194a7-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="194a7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="194a7-140">**IMF Media Event**</span><span class="sxs-lookup"><span data-stu-id="194a7-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="194a7-141">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="194a7-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="194a7-142">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="194a7-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



