---
title: Listen
description: Listen
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Listen
- Mischungen, Steuerelemente
- Mixer, Listen
- List-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- MIXERCONTROLDETAILS_LISTTEXT Struktur
- Steuerelement für die einfache Auswahl
- Mehrfachauswahl-Steuerelement
- Mixer-Steuerelement
- Multiplexer (MUX)
- MUX (Multiplexer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314780"
---
# <a name="lists"></a><span data-ttu-id="bf31c-115">Listen</span><span class="sxs-lookup"><span data-stu-id="bf31c-115">Lists</span></span>

<span data-ttu-id="bf31c-116">Die Listen-Steuerelemente stellen die einzelnen SELECT-und Multiple-Select-Zustände für komplexe audiozeilen bereit.</span><span class="sxs-lookup"><span data-stu-id="bf31c-116">The list controls provide single-select or multiple-select states for complex audio lines.</span></span> <span data-ttu-id="bf31c-117">Diese Steuerelemente verwenden die [**\_ boolesche "mixercontroldetails**](/previous-versions//dd757295(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bf31c-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="bf31c-118">Die " [**mixercontroldetails"- \_ listtext**](/previous-versions//dd757296(v=vs.85)) -Struktur wird auch verwendet, um alle Textbeschreibungen eines Steuer Elements mit mehreren Elementen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bf31c-118">The [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure is also used to retrieve all text descriptions of a multiple-item control.</span></span> <span data-ttu-id="bf31c-119">In der folgenden Tabelle werden die Typen von Listen Steuerelementen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bf31c-119">The following table describes the types of list controls.</span></span>



| <span data-ttu-id="bf31c-120">Control</span><span class="sxs-lookup"><span data-stu-id="bf31c-120">Control</span></span>           | <span data-ttu-id="bf31c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf31c-121">Description</span></span>                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31c-122">Einfache Auswahl</span><span class="sxs-lookup"><span data-stu-id="bf31c-122">Single-select</span></span>     | <span data-ttu-id="bf31c-123">Schränkt die Auswahl des Steuer Elements auf ein Element gleichzeitig ein.</span><span class="sxs-lookup"><span data-stu-id="bf31c-123">Restricts the control selection to one item at a time.</span></span> <span data-ttu-id="bf31c-124">Anders als das Multiplexer-Steuerelement kann dieses Steuerelement verwendet werden, um mehr als audioquellzeilen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="bf31c-124">Unlike the multiplexer control, this control can be used to control more than audio source lines.</span></span> <span data-ttu-id="bf31c-125">Beispielsweise können Sie mit diesem Steuerelement einen Tiefpass Filter aus einer Liste von Filtern auswählen, die von einem Mischungs Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bf31c-125">For example, you could use this control to select a low-pass filter from a list of filters supported by a mixer device.</span></span> |
| <span data-ttu-id="bf31c-126">Multiplexer (MUX)</span><span class="sxs-lookup"><span data-stu-id="bf31c-126">Multiplexer (MUX)</span></span> | <span data-ttu-id="bf31c-127">Schränkt die Zeilenauswahl auf jeweils eine Quellzeile ein.</span><span class="sxs-lookup"><span data-stu-id="bf31c-127">Restricts the line selection to one source line at a time.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="bf31c-128">Mehrfachauswahl</span><span class="sxs-lookup"><span data-stu-id="bf31c-128">Multiple-select</span></span>   | <span data-ttu-id="bf31c-129">Ermöglicht es dem Benutzer, mehrere Elemente gleichzeitig aus einer Liste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bf31c-129">Allows the user to select multiple items from a list simultaneously.</span></span> <span data-ttu-id="bf31c-130">Anders als das Mixer-Steuerelement kann das Mehrfachauswahl-Steuerelement verwendet werden, um mehr als audioquellzeilen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="bf31c-130">Unlike the mixer control, the multiple-select control can be used to control more than audio source lines.</span></span>                                                                                                  |
| <span data-ttu-id="bf31c-131">Mixer</span><span class="sxs-lookup"><span data-stu-id="bf31c-131">Mixer</span></span>             | <span data-ttu-id="bf31c-132">Ermöglicht dem Benutzer das gleichzeitige Auswählen von Quellzeilen aus einer Liste.</span><span class="sxs-lookup"><span data-stu-id="bf31c-132">Allows the user to select source lines from a list simultaneously.</span></span>                                                                                                                                                                                                               |



 

 

 