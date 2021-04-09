---
title: Switches
description: Switches
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Switches
- Mischungen, Steuerelemente
- Mixer, Switches
- Switch-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- Boolesches Steuerelement
- Button-Steuerelement
- ein/aus-Steuerelement
- Mono-Steuerelement
- Lautheit-Steuerelement
- Verbessertes Stereo Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858193"
---
# <a name="switches"></a><span data-ttu-id="e2ce1-115">Switches</span><span class="sxs-lookup"><span data-stu-id="e2ce1-115">Switches</span></span>

<span data-ttu-id="e2ce1-116">Die Switch-Steuerelemente sind Switches mit zwei Zuständen.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="e2ce1-117">Diese Steuerelemente verwenden die [**\_ boolesche "mixercontroldetails**](/previous-versions//dd757295(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="e2ce1-118">In der folgenden Tabelle werden die Typen von Switches beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="e2ce1-119">Control</span><span class="sxs-lookup"><span data-stu-id="e2ce1-119">Control</span></span>         | <span data-ttu-id="e2ce1-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2ce1-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ce1-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="e2ce1-121">Boolean</span></span>         | <span data-ttu-id="e2ce1-122">Der generische Switch.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-122">The generic switch.</span></span> <span data-ttu-id="e2ce1-123">Sie kann auf " **true** " oder " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="e2ce1-124">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="e2ce1-124">Button</span></span>          | <span data-ttu-id="e2ce1-125">Legen Sie für alle Schaltflächen, die vom Treiber behandelt werden sollen, den Wert " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="e2ce1-126">Wenn der Wert **false** ist, wird keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="e2ce1-127">Ein/Aus</span><span class="sxs-lookup"><span data-stu-id="e2ce1-127">On/Off</span></span>          | <span data-ttu-id="e2ce1-128">Ein alternativer Switch, der durch eine andere Grafik als die für den booleschen Switch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="e2ce1-129">Sie kann auf ein oder aus festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="e2ce1-130">Mute</span><span class="sxs-lookup"><span data-stu-id="e2ce1-130">Mute</span></span>            | <span data-ttu-id="e2ce1-131">Gibt eine Audiolinie an (unterdrückt den Datenfluss der Zeile) oder ermöglicht die Wiedergabe der Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="e2ce1-132">Dieser Schalter wird häufig verwendet, um die Zeilen zu steuern, die in den Mixer eingespeist werden.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="e2ce1-133">Mono</span><span class="sxs-lookup"><span data-stu-id="e2ce1-133">Mono</span></span>            | <span data-ttu-id="e2ce1-134">Schaltet zwischen Mono-und Stereoausgabe für eine Stereo Audiolinie um.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="e2ce1-135">Legen Sie diese Einstellung auf OFF fest, um Stereodaten als separate Kanäle wiederzugeben</span><span class="sxs-lookup"><span data-stu-id="e2ce1-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="e2ce1-136">Legen Sie auf ein fest, um Daten aus beiden Kanälen in eine Mono-Audiolinie zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="e2ce1-137">Lautstärke</span><span class="sxs-lookup"><span data-stu-id="e2ce1-137">Loudness</span></span>        | <span data-ttu-id="e2ce1-138">Steigert den Bass von niedrigem Volume für eine Audiolinie.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="e2ce1-139">Legen Sie auf ein fest, um den Bass von niedrigem Volume zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="e2ce1-140">Legen Sie diese Einstellung auf OFF fest, um die volumeebenen auf normal</span><span class="sxs-lookup"><span data-stu-id="e2ce1-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="e2ce1-141">Der Umfang der Verstärkung ist Hardware spezifisch.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="e2ce1-142">Weitere Informationen finden Sie in der Dokumentation für Ihr Mischgerät.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="e2ce1-143">Stereo-erweitert</span><span class="sxs-lookup"><span data-stu-id="e2ce1-143">Stereo Enhanced</span></span> | <span data-ttu-id="e2ce1-144">Vergrößert die Stereo Trennung.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-144">Increases stereo separation.</span></span> <span data-ttu-id="e2ce1-145">Legen Sie auf ein fest, um die Trennung von Stereo</span><span class="sxs-lookup"><span data-stu-id="e2ce1-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="e2ce1-146">Auf OFF festgelegt, um keine Erweiterung zu haben.</span><span class="sxs-lookup"><span data-stu-id="e2ce1-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 