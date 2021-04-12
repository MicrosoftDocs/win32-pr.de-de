---
title: Customslider-Element
description: Customslider-Element
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Windows Media Player Skins, customslider-Element
- Skins, customslider-Element
- Customslider-Element
- Verweis für Skins, customslider-Element
- Elemente, customslider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310479"
---
# <a name="customslider-element"></a><span data-ttu-id="80ee3-108">Customslider-Element</span><span class="sxs-lookup"><span data-stu-id="80ee3-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="80ee3-109">Das **customslider** -Element bietet eine Möglichkeit zum Erstellen und Bearbeiten eines Schieberegler-Steuer Elements beliebiger Form, z. b. eines kreisförmigen Knopfs.</span><span class="sxs-lookup"><span data-stu-id="80ee3-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="80ee3-110">Die folgenden Tabellen enthalten die Attribute und Ereignishandler, die von diesem Element unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="80ee3-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="80ee3-111">Das **customslider** -Element unterstützt die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="80ee3-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="80ee3-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="80ee3-112">Attribute</span></span>                                               | <span data-ttu-id="80ee3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80ee3-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80ee3-114">Cursor</span><span class="sxs-lookup"><span data-stu-id="80ee3-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="80ee3-115">Gibt den Wert des Schieberegler-Steuerelement Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über dem Schieberegler befindet</span><span class="sxs-lookup"><span data-stu-id="80ee3-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="80ee3-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="80ee3-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="80ee3-117">Gibt das Bild des Schiebereglers an, das verwendet wird, wenn der Schieberegler deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80ee3-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="80ee3-118">Windows Mage</span><span class="sxs-lookup"><span data-stu-id="80ee3-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="80ee3-119">Gibt das Bild des benutzerdefinierten Schiebereglers an oder ruft dieses ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="80ee3-120">hoverimage</span><span class="sxs-lookup"><span data-stu-id="80ee3-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="80ee3-121">Gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Maus über dem benutzerdefinierten Schieberegler befindet</span><span class="sxs-lookup"><span data-stu-id="80ee3-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="80ee3-122">image</span><span class="sxs-lookup"><span data-stu-id="80ee3-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="80ee3-123">Gibt den Namen der Datei an, die die den verschiedenen Zuständen des benutzerdefinierten Schiebereglers entsprechenden Bilder enthält, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="80ee3-124">max</span><span class="sxs-lookup"><span data-stu-id="80ee3-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="80ee3-125">Gibt den maximalen Wert des Bereichs an, der durch den benutzerdefinierten Schieberegler definiert ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="80ee3-126">min</span><span class="sxs-lookup"><span data-stu-id="80ee3-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="80ee3-127">Gibt den minimalen Wert des Bereichs an, der durch den benutzerdefinierten Schieberegler definiert ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="80ee3-128">positionImage</span><span class="sxs-lookup"><span data-stu-id="80ee3-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="80ee3-129">Gibt die ImageMap an oder ruft Sie ab, um zu bestimmen, welches Positions Bild aus der **Bilddatei** angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80ee3-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="80ee3-130">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="80ee3-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="80ee3-131">Gibt den QuickInfo-Text für den Schieberegler an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="80ee3-132">transparendcolor</span><span class="sxs-lookup"><span data-stu-id="80ee3-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="80ee3-133">Gibt die Transparenz Farbe der benutzerdefinierten Schieberegler-Bilder an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="80ee3-134">value</span><span class="sxs-lookup"><span data-stu-id="80ee3-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="80ee3-135">Gibt die aktuelle Position des Schiebereglers an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="80ee3-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="80ee3-136">Das **customslider** -Element kann die folgenden Ereignishandler implementieren.</span><span class="sxs-lookup"><span data-stu-id="80ee3-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="80ee3-137">Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="80ee3-137">Event handler</span></span>                                         | <span data-ttu-id="80ee3-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80ee3-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80ee3-139">ondragbegin</span><span class="sxs-lookup"><span data-stu-id="80ee3-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="80ee3-140">Behandelt ein Ereignis, das auftritt, wenn der Benutzer auf die linke Maustaste klickt und mit der Maus bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="80ee3-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="80ee3-141">ondragend</span><span class="sxs-lookup"><span data-stu-id="80ee3-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="80ee3-142">Behandelt ein Ereignis, das auftritt, wenn die linke Maustaste nach einem Zieh Vorgang losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="80ee3-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="80ee3-143">onpositionchange</span><span class="sxs-lookup"><span data-stu-id="80ee3-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="80ee3-144">Behandelt ein Ereignis, das auftritt, wenn sich die Position des Schiebereglers ändert, wenn der Benutzer auf klicken oder ziehen klickt.</span><span class="sxs-lookup"><span data-stu-id="80ee3-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="80ee3-145">Das **customslider** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren.</span><span class="sxs-lookup"><span data-stu-id="80ee3-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="80ee3-146">Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="80ee3-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80ee3-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80ee3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80ee3-148">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="80ee3-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




