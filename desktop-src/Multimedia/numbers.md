---
title: Zahlen (Windows Multimedia)
description: Zahlen
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Zahlen
- Mischungen, Steuerelemente
- Mixer, Zahlen
- Zahlen Steuerelemente
- MIXERCONTROLDETAILS_SIGNED Struktur
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Dezibelskala-Steuerelement
- Prozent Steuerelement
- signiertes Steuerelement
- nicht signiertes Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102671"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="17629-114">Zahlen (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="17629-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="17629-115">Die Anzahl der Steuerelemente ermöglicht dem Benutzer die Eingabe von numerischen Daten, die einer Zeile zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17629-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="17629-116">Die numerischen Daten werden als ganze Zahlen mit Vorzeichen, ganze Zahlen ohne Vorzeichen oder ganzzahlige Dezimalwerte ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="17629-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="17629-117">Diese Steuerelemente verwenden die " [**mixercontroldetails \_ Signed**](/previous-versions//dd757297(v=vs.85)) "-und " [**mixercontroldetails \_**](/previous-versions//dd757298(v=vs.85)) "-Struktur ohne Vorzeichen zum Abrufen und Festlegen von Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17629-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="17629-118">In der folgenden Tabelle werden die Typen von Zahlen Steuerelementen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="17629-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="17629-119">Control</span><span class="sxs-lookup"><span data-stu-id="17629-119">Control</span></span>  | <span data-ttu-id="17629-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17629-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17629-121">Signiert</span><span class="sxs-lookup"><span data-stu-id="17629-121">Signed</span></span>   | <span data-ttu-id="17629-122">Ermöglicht ganzzahlige Werte, die im Bereich von – 231 bis (231 – 1) eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17629-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="17629-123">Ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="17629-123">Unsigned</span></span> | <span data-ttu-id="17629-124">Ermöglicht ganzzahlige Werte, die im Bereich von 0 bis (232 – 1) eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17629-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="17629-125">Dezibelskala</span><span class="sxs-lookup"><span data-stu-id="17629-125">Decibel</span></span>  | <span data-ttu-id="17629-126">Ermöglicht das Eingeben von ganzzahligen Dezibelskala-Werten in Zehntel Dezimalstellen.</span><span class="sxs-lookup"><span data-stu-id="17629-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="17629-127">Der Wertebereich für dieses Steuerelement ist – 32.768 bis 32.767.</span><span class="sxs-lookup"><span data-stu-id="17629-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="17629-128">Percent</span><span class="sxs-lookup"><span data-stu-id="17629-128">Percent</span></span>  | <span data-ttu-id="17629-129">Ermöglicht die Eingabe von Werten als Prozentsätze.</span><span class="sxs-lookup"><span data-stu-id="17629-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
