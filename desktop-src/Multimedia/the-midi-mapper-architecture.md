---
title: Die Architektur der MIDI-Mapper
description: Die Architektur der MIDI-Mapper
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Architektur
- MIDI-Mapper, Setup Map
- Zuordnung zu einem MIDI
- MIDI-Mapper, Kanal Zuordnung
- MIDI-Mapper, patchmaps
- MIDI-Mapper, Schlüssel Zuordnungen
- Kanal Zuordnung
- patchzuordnungen
- Schlüssel Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310824"
---
# <a name="the-midi-mapper-architecture"></a><span data-ttu-id="be84d-114">Die Architektur der MIDI-Mapper</span><span class="sxs-lookup"><span data-stu-id="be84d-114">The MIDI Mapper Architecture</span></span>

<span data-ttu-id="be84d-115">Der MIDI-Mapper verwendet eine MIDI-Setup Zuordnung, um zu bestimmen, wie die empfangenen Nachrichten übersetzt und umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="be84d-115">The MIDI Mapper uses a MIDI setup map to determine how to translate and redirect the messages it receives.</span></span> <span data-ttu-id="be84d-116">Eine MIDI-Setup Zuordnung besteht aus den folgenden Typen von Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="be84d-116">A MIDI setup map consists of the following types of maps.</span></span>

-   [<span data-ttu-id="be84d-117">Die Kanal Zuordnung</span><span class="sxs-lookup"><span data-stu-id="be84d-117">The Channel Map</span></span>](the-channel-map.md)
-   [<span data-ttu-id="be84d-118">Patchzuordnungen</span><span class="sxs-lookup"><span data-stu-id="be84d-118">Patch Maps</span></span>](patch-maps.md)
-   [<span data-ttu-id="be84d-119">Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="be84d-119">Key Maps</span></span>](key-maps.md)

<span data-ttu-id="be84d-120">In der folgenden Abbildung werden die Rollen von Channel-, Patch-und Schlüssel Zuordnungen in einer Zuordnung von MIDI-Setup dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be84d-120">The following illustration shows the roles of channel, patch, and key maps in a MIDI setup map.</span></span>

![die Rollen von Channel-, Patch-und Key Maps in einem Paket Image der MIDI-Einrichtung](images/mmap-a02.gif)

 

 




