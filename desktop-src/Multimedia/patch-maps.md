---
title: Patchzuordnungen
description: Patchzuordnungen
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Digital Instrumentation Digital Interface (MIDI), MIDI-Mapper
- MIDI (Digital Instrumentation Digital Interface), MIDI-Mapper
- MIDI-Mapper, patchmaps
- patchzuordnungen
- 'MIDI-Programm: Änderungs Meldungen'
- MIDI-volumecontroller-Meldungen
- Programm-Änderungs Meldungen
- volumecontroller-Meldungen
- MIDI-Mapper, Programm-Änderungs Meldungen
- MIDI-Mapper, volumecontroller-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309851"
---
# <a name="patch-maps"></a><span data-ttu-id="48e0d-113">Patchzuordnungen</span><span class="sxs-lookup"><span data-stu-id="48e0d-113">Patch Maps</span></span>

<span data-ttu-id="48e0d-114">Jedem Kanal Zuordnungs Eintrag kann eine zugeordnete patchkarte zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="48e0d-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="48e0d-115">Patchzuordnungen wirken sich auf die Nachrichten von MIDI-Programmänderungen und Volume Controller aus.</span><span class="sxs-lookup"><span data-stu-id="48e0d-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="48e0d-116">Programm-Änderungs Meldungen weisen einen Synthesizer an, den instrumentierungsound (Patch) für einen angegebenen Kanal zu ändern.</span><span class="sxs-lookup"><span data-stu-id="48e0d-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="48e0d-117">Volumecontroller-Meldungen legen das Volume für einen Kanal fest.</span><span class="sxs-lookup"><span data-stu-id="48e0d-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="48e0d-118">Eine patchkarte verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128-Programm Änderungs Werte.</span><span class="sxs-lookup"><span data-stu-id="48e0d-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="48e0d-119">Jede patchzuordnung gibt Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="48e0d-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="48e0d-120">Ein Zielprogramm: Ändern Sie den Wert.</span><span class="sxs-lookup"><span data-stu-id="48e0d-120">A destination program-change value.</span></span>
-   <span data-ttu-id="48e0d-121">Ein volumeskalar.</span><span class="sxs-lookup"><span data-stu-id="48e0d-121">A volume scalar.</span></span> <span data-ttu-id="48e0d-122">(Weitere Informationen finden Sie [unter Volume Scalar](the-volume-scalar.md).)</span><span class="sxs-lookup"><span data-stu-id="48e0d-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="48e0d-123">Eine optionale Schlüssel Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="48e0d-123">An optional key map.</span></span> <span data-ttu-id="48e0d-124">(Weitere Informationen finden Sie unter [Key Maps](key-maps.md).)</span><span class="sxs-lookup"><span data-stu-id="48e0d-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="48e0d-125">Beim Empfang von Programm Änderungs Meldungen durch den MIDI-Mapper wird der Wert des Zielprogramms-ändern in der Nachricht durch den Wert für den Programm Änderungs Wert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="48e0d-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="48e0d-126">Wenn das Zielprogramm z. b. den Wert für Programmänderung 16 auf 18 festgelegt ist, ändert der MIDI-Mapper die Programm Änderungs Nachricht des Pakets, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="48e0d-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![Bild von MIDI-Mapper](images/mmap-a03.gif)

 

 




