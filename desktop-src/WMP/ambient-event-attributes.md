---
title: Ambient-Ereignis Attribute
description: Ambient-Ereignis Attribute
ms.assetid: 56cd2701-53b3-4456-8fcd-d65f8a6aefd7
keywords:
- Windows Media Player Skins, Ambient-Ereignis Attribute
- Skins, Ambient-Ereignis Attribute
- Referenz für Skins, Ambient-Ereignis Attribute
- Ambient-Ereignis Attribute
- Attribute, Ambient-Ereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40522a741509e56d2e4c9201c305126067a0fe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708735"
---
# <a name="ambient-event-attributes"></a><span data-ttu-id="9f5de-108">Ambient-Ereignis Attribute</span><span class="sxs-lookup"><span data-stu-id="9f5de-108">Ambient Event Attributes</span></span>

<span data-ttu-id="9f5de-109">Die folgenden Attribute sind für alle Skin-Ereignisse üblich.</span><span class="sxs-lookup"><span data-stu-id="9f5de-109">The following attributes are common to all skin events.</span></span> <span data-ttu-id="9f5de-110">Der Zugriff erfolgt über das Schlüsselwort " **Event** " innerhalb eines Ereignis Handlers für das-Element.</span><span class="sxs-lookup"><span data-stu-id="9f5de-110">They are accessed with the **event** keyword within an event handler for the element.</span></span>



| <span data-ttu-id="9f5de-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="9f5de-111">Attribute</span></span>                              | <span data-ttu-id="9f5de-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f5de-112">Description</span></span>                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f5de-113">altKey</span><span class="sxs-lookup"><span data-stu-id="9f5de-113">altKey</span></span>](event-altkey.md)             | <span data-ttu-id="9f5de-114">Ruft einen Wert ab, der angibt, ob die Alt-Taste gedrückt wurde, als das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f5de-114">Retrieves a value indicating whether the ALT key was down when the event occurred.</span></span>                           |
| [<span data-ttu-id="9f5de-115">gedrückt</span><span class="sxs-lookup"><span data-stu-id="9f5de-115">button</span></span>](event-button.md)             | <span data-ttu-id="9f5de-116">Ruft einen Wert ab, der angibt, welche Maustasten beim Eintreten des Ereignisses angezeigt wurden.</span><span class="sxs-lookup"><span data-stu-id="9f5de-116">Retrieves a value indicating which mouse buttons were down when the event occurred.</span></span>                          |
| [<span data-ttu-id="9f5de-117">clientX</span><span class="sxs-lookup"><span data-stu-id="9f5de-117">clientX</span></span>](event-clientx.md)           | <span data-ttu-id="9f5de-118">Ruft die x-Koordinate des Mauszeigers in Bezug auf den Client Bereich des Anwendungsfensters ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-118">Retrieves the x-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="9f5de-119">clientY</span><span class="sxs-lookup"><span data-stu-id="9f5de-119">clientY</span></span>](event-clienty.md)           | <span data-ttu-id="9f5de-120">Ruft die y-Koordinate des Mauszeigers in Bezug auf den Client Bereich des Anwendungsfensters ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-120">Retrieves the y-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="9f5de-121">ctrlKey</span><span class="sxs-lookup"><span data-stu-id="9f5de-121">ctrlKey</span></span>](event-ctrlkey.md)           | <span data-ttu-id="9f5de-122">Ruft einen Wert ab, der angibt, ob die STRG-Taste gedrückt wurde, als das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f5de-122">Retrieves a value indicating whether the CTRL key was down when the event occurred.</span></span>                          |
| [<span data-ttu-id="9f5de-123">fromelements</span><span class="sxs-lookup"><span data-stu-id="9f5de-123">fromElement</span></span>](event-fromelement.md)   | <span data-ttu-id="9f5de-124">Ruft das Element ab, von dem das Ereignis stammt.</span><span class="sxs-lookup"><span data-stu-id="9f5de-124">Retrieves the element the event came from.</span></span>                                                                   |
| [<span data-ttu-id="9f5de-125">Keycode</span><span class="sxs-lookup"><span data-stu-id="9f5de-125">keyCode</span></span>](event-keycode.md)           | <span data-ttu-id="9f5de-126">Ruft den ASCII-Schlüsselcode ab, wenn eine Taste gedrückt wurde, als das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f5de-126">Retrieves the ASCII key code if a key was pressed when the event occurred.</span></span>                                   |
| [<span data-ttu-id="9f5de-127">OffsetX</span><span class="sxs-lookup"><span data-stu-id="9f5de-127">offsetX</span></span>](event-offsetx.md)           | <span data-ttu-id="9f5de-128">Ruft die x-Koordinate des Mauszeigers in Bezug auf das Element ab, das das Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="9f5de-128">Retrieves the x-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="9f5de-129">offität</span><span class="sxs-lookup"><span data-stu-id="9f5de-129">offsetY</span></span>](event-offsety.md)           | <span data-ttu-id="9f5de-130">Ruft die y-Koordinate des Mauszeigers in Bezug auf das Element ab, das das Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="9f5de-130">Retrieves the y-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="9f5de-131">ScreenHeight</span><span class="sxs-lookup"><span data-stu-id="9f5de-131">screenHeight</span></span>](event-screenheight.md) | <span data-ttu-id="9f5de-132">Ruft die Höhe der verfügbaren Bildschirmgröße in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-132">Retrieves the height of the available screen size in pixels.</span></span>                                                 |
| [<span data-ttu-id="9f5de-133">Bildschirmbreite</span><span class="sxs-lookup"><span data-stu-id="9f5de-133">screenWidth</span></span>](event-screenwidth.md)   | <span data-ttu-id="9f5de-134">Ruft die Breite der verfügbaren Bildschirmgröße in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-134">Retrieves the width of the available screen size in pixels.</span></span>                                                  |
| [<span data-ttu-id="9f5de-135">screenX</span><span class="sxs-lookup"><span data-stu-id="9f5de-135">screenX</span></span>](event-screenx.md)           | <span data-ttu-id="9f5de-136">Ruft die absolute x-Koordinate des Mauszeigers in Bezug auf den Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-136">Retrieves the absolute x-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="9f5de-137">Screeny</span><span class="sxs-lookup"><span data-stu-id="9f5de-137">screenY</span></span>](event-screeny.md)           | <span data-ttu-id="9f5de-138">Ruft die absolute y-Koordinate des Mauszeigers in Bezug auf den Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-138">Retrieves the absolute y-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="9f5de-139">shiftKey</span><span class="sxs-lookup"><span data-stu-id="9f5de-139">shiftKey</span></span>](event-shiftkey.md)         | <span data-ttu-id="9f5de-140">Ruft einen Wert ab, der angibt, ob die UMSCHALTTASTE gedrückt wurde, als das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f5de-140">Retrieves a value indicating whether the SHIFT key was down when the event occurred.</span></span>                         |
| [<span data-ttu-id="9f5de-141">srcelements</span><span class="sxs-lookup"><span data-stu-id="9f5de-141">srcElement</span></span>](event-srcelement.md)     | <span data-ttu-id="9f5de-142">Ruft das Element ab, das das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="9f5de-142">Retrieves the element that fired the event.</span></span>                                                                  |
| [<span data-ttu-id="9f5de-143">"Element"</span><span class="sxs-lookup"><span data-stu-id="9f5de-143">toElement</span></span>](event-toelement.md)       | <span data-ttu-id="9f5de-144">Ruft das Element ab, zu dem der Tastaturfokus verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="9f5de-144">Retrieves the element the keyboard focus moved to.</span></span>                                                           |
| [<span data-ttu-id="9f5de-145">x</span><span class="sxs-lookup"><span data-stu-id="9f5de-145">x</span></span>](event-x.md)                       | <span data-ttu-id="9f5de-146">Ruft die x-Koordinate des Mauszeigers in Bezug auf das Anwendungsfenster ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-146">Retrieves the x-coordinate of the mouse pointer with respect to the application window.</span></span>                      |
| [<span data-ttu-id="9f5de-147">y</span><span class="sxs-lookup"><span data-stu-id="9f5de-147">y</span></span>](event-y.md)                       | <span data-ttu-id="9f5de-148">Ruft die y-Koordinate des Mauszeigers in Bezug auf das Anwendungsfenster ab.</span><span class="sxs-lookup"><span data-stu-id="9f5de-148">Retrieves the y-coordinate of the mouse pointer with respect to the application window.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="9f5de-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f5de-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f5de-150">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="9f5de-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




