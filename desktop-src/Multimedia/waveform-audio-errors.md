---
title: Waveform-Audio Fehler
description: Waveform-Audio Fehler
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Mcierr-Rückgabewerte, Waveform-Audiofehler
- Multimedia-Referenz, Waveform-Audiofehler
- Referenz für Multimedia-, Waveform-Audiofehler
- Media Control Interface (MCI), Waveform-Audiofehler
- MCI (Medien Steuerungs Schnittstelle), Waveform-Audiofehler
- Referenz für MCI, Waveform-Audiofehler
- MCI-Referenz, Waveform-Audiofehler
- Media Control Interface (MCI), Fehler
- MCI (Medien Steuerungs Schnittstelle), Fehler
- Referenz für MCI, Fehler
- MCI-Referenz, Fehler
- Waveform-Audiofehler
- MCI-Waveform-Audiofehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036557"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="8843a-116">Waveform-Audio Fehler</span><span class="sxs-lookup"><span data-stu-id="8843a-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="8843a-117">Die folgenden zusätzlichen Rückgabewerte werden für MCI-Waveform-Audiogeräte definiert:</span><span class="sxs-lookup"><span data-stu-id="8843a-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="8843a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8843a-118">Value</span></span>                             | <span data-ttu-id="8843a-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8843a-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8843a-120">mcierr \_ Wave \_ inputsinuse</span><span class="sxs-lookup"><span data-stu-id="8843a-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="8843a-121">Alle Wellenform-Geräte, die Dateien im aktuellen Format aufzeichnen können, werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="8843a-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="8843a-122">Warten Sie, bis eines dieser Geräte kostenlos ist. versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="8843a-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="8843a-123">mcierr \_ Wave \_ inputsungeeig</span><span class="sxs-lookup"><span data-stu-id="8843a-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="8843a-124">Kein installiertes Wellenform-Gerät kann Dateien im aktuellen Format aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="8843a-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="8843a-125">Verwenden Sie die Option Drivers in der Systemsteuerung, um ein geeignetes Wellen Formular-Aufzeichnungsgerät zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8843a-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="8843a-126">mcierr \_ Wave \_ inputunspezifiziert</span><span class="sxs-lookup"><span data-stu-id="8843a-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="8843a-127">Sie können ein beliebiges kompatibles Wellen Formular-Aufzeichnungsgerät angeben.</span><span class="sxs-lookup"><span data-stu-id="8843a-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="8843a-128">mcierr \_ Wave \_ outputsinuse</span><span class="sxs-lookup"><span data-stu-id="8843a-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="8843a-129">Alle Wellenform-Geräte, die Dateien im aktuellen Format wiedergeben können, werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="8843a-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="8843a-130">Warten Sie, bis eines dieser Geräte kostenlos ist. versuchen Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="8843a-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="8843a-131">mcierr \_ Wave \_ outputsunpassend</span><span class="sxs-lookup"><span data-stu-id="8843a-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="8843a-132">Kein installiertes Wellenform-Gerät kann Dateien im aktuellen Format wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="8843a-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="8843a-133">Verwenden Sie die Option Drivers in der Systemsteuerung, um ein geeignetes Wellenform-Gerät zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8843a-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="8843a-134">mcierr \_ Wave \_ outputunspezifiziert</span><span class="sxs-lookup"><span data-stu-id="8843a-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="8843a-135">Sie können ein beliebiges kompatibles Wellenform Wiedergabe Gerät angeben.</span><span class="sxs-lookup"><span data-stu-id="8843a-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="8843a-136">mcierr \_ Wave \* \_ tinputinuse</span><span class="sxs-lookup"><span data-stu-id="8843a-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="8843a-137">Das aktuelle Wellenform-Gerät wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="8843a-137">The current waveform device is in use.</span></span> <span data-ttu-id="8843a-138">Warten Sie, bis das Gerät kostenlos ist. versuchen Sie dann erneut, das Gerät für die Aufzeichnung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8843a-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="8843a-139">mcierr \_ Wave \* \_ tinputungeeignet</span><span class="sxs-lookup"><span data-stu-id="8843a-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="8843a-140">Das Gerät, das Sie verwenden, um eine Wellenform aufzuzeichnen, kann das Datenformat nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="8843a-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="8843a-141">mcierr \_ Wave \_ setoutputinuse</span><span class="sxs-lookup"><span data-stu-id="8843a-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="8843a-142">Das aktuelle Wellenform-Gerät wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="8843a-142">The current waveform device is in use.</span></span> <span data-ttu-id="8843a-143">Warten Sie, bis das Gerät kostenlos ist. versuchen Sie dann erneut, das Gerät für die Wiedergabe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8843a-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="8843a-144">mcierr \_ Wave \_ setoutputungeeignet</span><span class="sxs-lookup"><span data-stu-id="8843a-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="8843a-145">Das Gerät, das Sie verwenden, um eine Wellenform wiederzugeben, kann das Datenformat nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="8843a-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




