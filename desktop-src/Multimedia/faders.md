---
title: Faders
description: Faders
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Faders
- Mischungen, Steuerelemente
- Mixer, Faders
- Faders
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Volume Fade-Steuerelement
- Bass Volume-Fade-Steuerelement
- Steuerelement für Aufblenden von Volumes
- Grafik-Ausgleichs Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948637"
---
# <a name="faders"></a><span data-ttu-id="0fd45-113">Faders</span><span class="sxs-lookup"><span data-stu-id="0fd45-113">Faders</span></span>

<span data-ttu-id="0fd45-114">Die Fader-Steuerelemente sind in der Regel vertikale Steuerelemente, die nach oben oder unten angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="0fd45-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="0fd45-115">Diese Steuerelemente verfügen über eine lineare Skala und verwenden die " [**mixercontroldetails \_**](/previous-versions//dd757298(v=vs.85)) "-Struktur ohne Vorzeichen zum Abrufen und Festlegen von Steuerelement Details.</span><span class="sxs-lookup"><span data-stu-id="0fd45-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="0fd45-116">In der folgenden Tabelle werden die Typen von Faders beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0fd45-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="0fd45-117">Control</span><span class="sxs-lookup"><span data-stu-id="0fd45-117">Control</span></span>   | <span data-ttu-id="0fd45-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fd45-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd45-119">Fader</span><span class="sxs-lookup"><span data-stu-id="0fd45-119">Fader</span></span>     | <span data-ttu-id="0fd45-120">Allgemeines Fade-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fd45-120">General fade control.</span></span> <span data-ttu-id="0fd45-121">Der Bereich zulässiger Werte ist 0 bis 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fd45-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0fd45-122">Lautstärke</span><span class="sxs-lookup"><span data-stu-id="0fd45-122">Volume</span></span>    | <span data-ttu-id="0fd45-123">Allgemeines Volumen-Fade-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fd45-123">General volume fade control.</span></span> <span data-ttu-id="0fd45-124">Der Bereich zulässiger Werte ist 0 bis 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fd45-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0fd45-125">Informationen zum Ändern dieses Bereichs finden Sie in der Dokumentation für Ihr Mischgerät.</span><span class="sxs-lookup"><span data-stu-id="0fd45-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="0fd45-126">Barsch</span><span class="sxs-lookup"><span data-stu-id="0fd45-126">Bass</span></span>      | <span data-ttu-id="0fd45-127">Bass Volume-Fade-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fd45-127">Bass volume fade control.</span></span> <span data-ttu-id="0fd45-128">Der Bereich zulässiger Werte ist 0 bis 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fd45-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0fd45-129">Die Grenzwerte für das Bass Frequenzband sind Hardware spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0fd45-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="0fd45-130">Informationen zu Band Limits finden Sie in der Dokumentation für Ihr Mischgerät.</span><span class="sxs-lookup"><span data-stu-id="0fd45-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0fd45-131">Höhen</span><span class="sxs-lookup"><span data-stu-id="0fd45-131">Treble</span></span>    | <span data-ttu-id="0fd45-132">Gespeicherbare volumefade-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fd45-132">Treble volume fade control.</span></span> <span data-ttu-id="0fd45-133">Der Bereich zulässiger Werte ist 0 bis 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fd45-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="0fd45-134">Die Grenzwerte für das Höhen Frequency-Band sind Hardware spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0fd45-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="0fd45-135">Informationen zu den Band Limits finden Sie in der Dokumentation für Ihr Mischgerät.</span><span class="sxs-lookup"><span data-stu-id="0fd45-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="0fd45-136">Equalizer</span><span class="sxs-lookup"><span data-stu-id="0fd45-136">Equalizer</span></span> | <span data-ttu-id="0fd45-137">Grafik-equalikansteuerelement.</span><span class="sxs-lookup"><span data-stu-id="0fd45-137">Graphic equalizer control.</span></span> <span data-ttu-id="0fd45-138">Der Bereich der zulässigen Werte für ein Band des Equalizers liegt zwischen 0 und 65.535.</span><span class="sxs-lookup"><span data-stu-id="0fd45-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="0fd45-139">Die Anzahl der Ausgleichs Bänder und ihre Grenzwerte sind Hardware spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0fd45-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="0fd45-140">Weitere Informationen zum Equalizer finden Sie in der Dokumentation für Ihr Mischgerät.</span><span class="sxs-lookup"><span data-stu-id="0fd45-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="0fd45-141">Sie können die [**\_ listtext-Struktur mixercontroldetails**](/previous-versions//dd757296(v=vs.85)) verwenden, um Text Bezeichnungen für den Equalizer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0fd45-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 