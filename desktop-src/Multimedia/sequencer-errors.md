---
title: Sequencer-Fehler
description: Sequencer-Fehler
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Mcierr-Rückgabewerte, Sequencer-Fehler
- Multimedia-Referenz, Sequencer-Fehler
- Referenz für Multimedia-, Sequencer-Fehler
- Media Control Interface (MCI), Sequencer-Fehler
- MCI (Medien Steuerungs Schnittstelle), Sequencer-Fehler
- Referenz für MCI, Sequencer-Fehler
- MCI-Referenz, Sequencer-Fehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Sequencer-Fehler
- MCI-Sequencer-Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710440"
---
# <a name="sequencer-errors"></a><span data-ttu-id="6f19b-116">Sequencer-Fehler</span><span class="sxs-lookup"><span data-stu-id="6f19b-116">Sequencer Errors</span></span>

<span data-ttu-id="6f19b-117">Die folgenden zusätzlichen Rückgabewerte werden für MCI-Sequencer definiert:</span><span class="sxs-lookup"><span data-stu-id="6f19b-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="6f19b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6f19b-118">Value</span></span>                          | <span data-ttu-id="6f19b-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f19b-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f19b-120">mcierr, nicht \_ \_ \_ kompatibel</span><span class="sxs-lookup"><span data-stu-id="6f19b-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="6f19b-121">Die Zeitformate von "Song Pointer" und "SMPTE" sind Singular.</span><span class="sxs-lookup"><span data-stu-id="6f19b-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="6f19b-122">Sie können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f19b-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="6f19b-123">mcierr/ \_ q- \_ nomidipresent</span><span class="sxs-lookup"><span data-stu-id="6f19b-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="6f19b-124">Dieses System verfügt über keine installierten MIDI-Geräte.</span><span class="sxs-lookup"><span data-stu-id="6f19b-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="6f19b-125">Verwenden Sie die Option Drivers in der Systemsteuerung, um einen MIDI-Treiber zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6f19b-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="6f19b-126">mcierr- \_ \_ Port- \_ InUse</span><span class="sxs-lookup"><span data-stu-id="6f19b-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="6f19b-127">Der angegebene MIDI-Port wird bereits verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f19b-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="6f19b-128">Warten Sie, bis der Vorgang kostenlos ist. versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="6f19b-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="6f19b-129">mcierr/ \_ q- \_ Port \_ mapnodevice</span><span class="sxs-lookup"><span data-stu-id="6f19b-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="6f19b-130">Das aktuelle Installationsprogramm für das MIDI-Mapper bezieht sich auf ein auf dem System nicht installiertes MIDI-Gerät.</span><span class="sxs-lookup"><span data-stu-id="6f19b-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="6f19b-131">Verwenden Sie den System Steuerungs-Mapper in der Systemsteuerung, um das Setup zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f19b-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="6f19b-132">Fehler beim mcierr- \_ /q- \_ Port. \_</span><span class="sxs-lookup"><span data-stu-id="6f19b-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="6f19b-133">Fehler beim angegebenen Port.</span><span class="sxs-lookup"><span data-stu-id="6f19b-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="6f19b-134">mcierr- \_ \_ Port ist \_ nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6f19b-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="6f19b-135">Das angegebene MIDI-Gerät ist nicht auf dem System installiert.</span><span class="sxs-lookup"><span data-stu-id="6f19b-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="6f19b-136">Verwenden Sie die Option Drivers in der Systemsteuerung, um ein MIDI-Gerät zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6f19b-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="6f19b-137">\_nicht spezifizierter mcierr- \_ Port</span><span class="sxs-lookup"><span data-stu-id="6f19b-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="6f19b-138">Das System verfügt über keinen aktuellen, von Ihnen angegebenen MIDI-Port.</span><span class="sxs-lookup"><span data-stu-id="6f19b-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="6f19b-139">mcierr-Zeit Geber \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f19b-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="6f19b-140">Alle Multimediatimer werden von anderen Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f19b-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="6f19b-141">Beenden Sie eine dieser Anwendungen. versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="6f19b-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 




