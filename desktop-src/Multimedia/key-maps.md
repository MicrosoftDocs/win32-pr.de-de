---
title: Schlüssel Zuordnungen
description: Schlüssel Zuordnungen
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, Schlüssel Zuordnungen
- Schlüssel Zuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947567"
---
# <a name="key-maps"></a><span data-ttu-id="5d5c7-107">Schlüssel Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="5d5c7-107">Key Maps</span></span>

<span data-ttu-id="5d5c7-108">Jedem Eintrag in der patchzuordnungs-Übersetzungstabelle ist eine zugeordnete Schlüssel Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5d5c7-108">Each entry in the patch-map translation table can have an associated key map.</span></span> <span data-ttu-id="5d5c7-109">Schlüssel Zuordnungen betreffen die Nachrichten "Note-on", "Note-Off" und "Polyphonic-after-afternote".</span><span class="sxs-lookup"><span data-stu-id="5d5c7-109">Key maps affect note-on, note-off, and polyphonic-key-aftertouch messages.</span></span> <span data-ttu-id="5d5c7-110">Eine Schlüssel Zuordnung verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128-Schlüsselwerte.</span><span class="sxs-lookup"><span data-stu-id="5d5c7-110">A key map has a translation table with an entry for each of the 128 MIDI key values.</span></span> <span data-ttu-id="5d5c7-111">Wenn der Eintrag für den Schlüsselwert 60 z. b. 72 ist, ändert der MIDI-Mapper die Informationen zu "MIDI Note-on", wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5d5c7-111">For example, if the entry for key value 60 is 72, the MIDI Mapper modifies MIDI note-on messages as shown in the following illustration.</span></span>

![Bild von MIDI-Mapper](images/mmap-a06.gif)

<span data-ttu-id="5d5c7-113">Schlüssel Zuordnungen sind bei Synthesizern nützlich, die über Schlüssel basierte Percussion-Instrumente verfügen, denen jeweils ein bestimmter Percussion-Sound zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5d5c7-113">Key maps are useful with synthesizers that have key-based percussion instruments with a particular percussion sound assigned to each key.</span></span> <span data-ttu-id="5d5c7-114">Schlüssel Zuordnungen werden in der Regel dem ersten Patch in den patchmaps auf den Percussion-Kanälen (10 und 16) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="5d5c7-114">Key maps are usually assigned to the first patch in the patch maps on the percussion channels (10 and 16).</span></span>

 

 




