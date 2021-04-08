---
title: Zusammenfassung der Maps-und MIDI-Meldungen
description: Zusammenfassung der Maps-und MIDI-Meldungen
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Kanal Zuordnung
- MIDI-Mapper, patchmaps
- MIDI-Mapper, Schlüssel Zuordnungen
- Kanal Zuordnung
- patchzuordnungen
- Schlüssel Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713302"
---
# <a name="summary-of-maps-and-midi-messages"></a><span data-ttu-id="e8855-111">Zusammenfassung der Maps-und MIDI-Meldungen</span><span class="sxs-lookup"><span data-stu-id="e8855-111">Summary of Maps and MIDI Messages</span></span>

<span data-ttu-id="e8855-112">Im folgenden finden Sie die Status Bytes für MIDI-Nachrichten und die Zuordnungs Typen, die jede Nachricht beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="e8855-112">Following are the status bytes for MIDI messages and the map types that affect each message.</span></span>



| <span data-ttu-id="e8855-113">Status von MIDI</span><span class="sxs-lookup"><span data-stu-id="e8855-113">MIDI status</span></span> | <span data-ttu-id="e8855-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8855-114">Description</span></span>               | <span data-ttu-id="e8855-115">Kartentypen</span><span class="sxs-lookup"><span data-stu-id="e8855-115">Map types</span></span>                |
|-------------|---------------------------|--------------------------|
| <span data-ttu-id="e8855-116">0x80-0x8F</span><span class="sxs-lookup"><span data-stu-id="e8855-116">0x80-0x8F</span></span>   | <span data-ttu-id="e8855-117">Notiz aus</span><span class="sxs-lookup"><span data-stu-id="e8855-117">Note off</span></span>                  | <span data-ttu-id="e8855-118">Kanal Zuordnungen, Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e8855-118">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e8855-119">0x90-0x9F</span><span class="sxs-lookup"><span data-stu-id="e8855-119">0x90-0x9F</span></span>   | <span data-ttu-id="e8855-120">Hinweis zu </span><span class="sxs-lookup"><span data-stu-id="e8855-120">Note on</span></span>                   | <span data-ttu-id="e8855-121">Kanal Zuordnungen, Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e8855-121">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e8855-122">0xa0-0xaf</span><span class="sxs-lookup"><span data-stu-id="e8855-122">0xA0-0xAF</span></span>   | <span data-ttu-id="e8855-123">Polyonic-Schlüssel-afterberührungs</span><span class="sxs-lookup"><span data-stu-id="e8855-123">Polyphonic-key aftertouch</span></span> | <span data-ttu-id="e8855-124">Kanal Zuordnungen, Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e8855-124">Channel maps, key maps</span></span>   |
| <span data-ttu-id="e8855-125">0xb0-0xBF</span><span class="sxs-lookup"><span data-stu-id="e8855-125">0xB0-0xBF</span></span>   | <span data-ttu-id="e8855-126">Steuerelement Änderung</span><span class="sxs-lookup"><span data-stu-id="e8855-126">Control change</span></span>            | <span data-ttu-id="e8855-127">Kanal Zuordnungen, patchmaps</span><span class="sxs-lookup"><span data-stu-id="e8855-127">Channel maps, patch maps</span></span> |
| <span data-ttu-id="e8855-128">0xc0-0xCF</span><span class="sxs-lookup"><span data-stu-id="e8855-128">0xC0-0xCF</span></span>   | <span data-ttu-id="e8855-129">Programmänderung</span><span class="sxs-lookup"><span data-stu-id="e8855-129">Program change</span></span>            | <span data-ttu-id="e8855-130">Kanal Zuordnungen, patchmaps</span><span class="sxs-lookup"><span data-stu-id="e8855-130">Channel maps, patch maps</span></span> |
| <span data-ttu-id="e8855-131">0xd0-0xDF</span><span class="sxs-lookup"><span data-stu-id="e8855-131">0xD0-0xDF</span></span>   | <span data-ttu-id="e8855-132">Kanal-afterberührungs</span><span class="sxs-lookup"><span data-stu-id="e8855-132">Channel aftertouch</span></span>        | <span data-ttu-id="e8855-133">Kanal Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e8855-133">Channel maps</span></span>             |
| <span data-ttu-id="e8855-134">0xe0-0xEF</span><span class="sxs-lookup"><span data-stu-id="e8855-134">0xE0-0xEF</span></span>   | <span data-ttu-id="e8855-135">Änderung der ebenumkurve</span><span class="sxs-lookup"><span data-stu-id="e8855-135">Pitch-bend change</span></span>         | <span data-ttu-id="e8855-136">Kanal Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="e8855-136">Channel maps</span></span>             |
| <span data-ttu-id="e8855-137">0xF 0-0xFF</span><span class="sxs-lookup"><span data-stu-id="e8855-137">0xF0-0xFF</span></span>   | <span data-ttu-id="e8855-138">System</span><span class="sxs-lookup"><span data-stu-id="e8855-138">System</span></span>                    | <span data-ttu-id="e8855-139">Nicht zugeordnet</span><span class="sxs-lookup"><span data-stu-id="e8855-139">Not mapped</span></span>               |



 

-   <span data-ttu-id="e8855-140">Die hochwertigen vier Bits stellen den Statuswert dar.</span><span class="sxs-lookup"><span data-stu-id="e8855-140">The high-order four bits represent the status value.</span></span> <span data-ttu-id="e8855-141">Die nieder wertigen vier Bits stellen die Kanalinformationen dar.</span><span class="sxs-lookup"><span data-stu-id="e8855-141">The low-order four bits represent the channel information.</span></span>
-   <span data-ttu-id="e8855-142">Patchmaps wirken sich nur auf Controller 7 (Haupt Volume) aus.</span><span class="sxs-lookup"><span data-stu-id="e8855-142">Patch maps affect only controller 7 (main volume).</span></span>
-   <span data-ttu-id="e8855-143">System Meldungen werden an alle Geräte gesendet, die in einer Kanal Zuordnung aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e8855-143">System messages are sent to all devices listed in a channel map.</span></span>

 

 




