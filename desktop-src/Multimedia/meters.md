---
title: Meter
description: Meter
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Meter
- Mischungen, Steuerelemente
- Mixer, Meter
- Mess Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- MIXERCONTROLDETAILS_SIGNED Struktur
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Boolesches Steuerelement
- Spitzen Kontrolle
- signiertes Steuerelement
- nicht signiertes Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473116"
---
# <a name="meters"></a><span data-ttu-id="593b5-115">Meter</span><span class="sxs-lookup"><span data-stu-id="593b5-115">Meters</span></span>

<span data-ttu-id="593b5-116">Die Mess Steuerelemente messen die Daten, die über eine audiozeile übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="593b5-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="593b5-117">Diese Steuerelemente verwenden den [**mixercontroldetails- \_ booleschen**](/previous-versions//dd757295(v=vs.85))Wert, [**mixercontroldetails \_ signiert**](/previous-versions//dd757297(v=vs.85))und [**mixercontroldetails \_ nicht signierte**](/previous-versions//dd757298(v=vs.85)) Strukturen zum Abrufen und Festlegen von Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="593b5-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="593b5-118">In der folgenden Tabelle werden die Typen von Zählern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="593b5-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="593b5-119">Control</span><span class="sxs-lookup"><span data-stu-id="593b5-119">Control</span></span>  | <span data-ttu-id="593b5-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="593b5-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="593b5-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="593b5-121">Boolean</span></span>  | <span data-ttu-id="593b5-122">Misst, ob ein ganzzahliger Wert false/Off (null) oder true/on (ungleich null) ist.</span><span class="sxs-lookup"><span data-stu-id="593b5-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="593b5-123">Peak</span><span class="sxs-lookup"><span data-stu-id="593b5-123">Peak</span></span>     | <span data-ttu-id="593b5-124">Misst die Ablenkung von 0 in der positiven und negativen Richtung.</span><span class="sxs-lookup"><span data-stu-id="593b5-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="593b5-125">Der Bereich der ganzzahligen Werte für die Spitzen Meter beträgt – 32.768 bis 32.767.</span><span class="sxs-lookup"><span data-stu-id="593b5-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="593b5-126">Signiert</span><span class="sxs-lookup"><span data-stu-id="593b5-126">Signed</span></span>   | <span data-ttu-id="593b5-127">Misst ganzzahlige Werte im Bereich von – 231 bis (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="593b5-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="593b5-128">Der mischertreibers definiert die Grenzwerte dieser Verbrauchseinheit.</span><span class="sxs-lookup"><span data-stu-id="593b5-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="593b5-129">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="593b5-129">Unsigned</span></span> | <span data-ttu-id="593b5-130">Misst ganzzahlige Werte im Bereich von 0 bis (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="593b5-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="593b5-131">Der mischertreibers definiert die Grenzwerte dieser Verbrauchseinheit.</span><span class="sxs-lookup"><span data-stu-id="593b5-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 