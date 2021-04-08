---
title: Video-Element
description: Video-Element
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player Skins, Video-Element
- Skins, Video-Element
- Video-Element
- Verweis für Skins, Video-Element
- Elemente, Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711105"
---
# <a name="video-element"></a><span data-ttu-id="667fb-108">Video-Element</span><span class="sxs-lookup"><span data-stu-id="667fb-108">VIDEO Element</span></span>

<span data-ttu-id="667fb-109">Das **Video** -Element bietet eine Möglichkeit, ein Video Fenster in einer Skin zu bearbeiten, indem die folgenden Attribute und Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="667fb-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="667fb-110">Ein vordefiniertes **Video** Element wird auch zur einfacheren Bereitstellung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="667fb-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="667fb-111">Das **Video** -Element unterstützt die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="667fb-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="667fb-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="667fb-112">Attribute</span></span>                                            | <span data-ttu-id="667fb-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="667fb-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="667fb-114">Background Color</span><span class="sxs-lookup"><span data-stu-id="667fb-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="667fb-115">Gibt die Hintergrundfarbe des Video Steuer Elements an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="667fb-116">Cursor</span><span class="sxs-lookup"><span data-stu-id="667fb-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="667fb-117">Gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="667fb-118">Vollbild</span><span class="sxs-lookup"><span data-stu-id="667fb-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="667fb-119">Gibt einen Wert an, der angibt, ob das Video im Vollbildmodus angezeigt wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="667fb-120">Kann nur zur Laufzeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="667fb-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="667fb-121">wart AspectRatio</span><span class="sxs-lookup"><span data-stu-id="667fb-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="667fb-122">Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob im Video das Seitenverhältnis beibehalten wird, wenn versucht wird, die Breite und Höhe des Steuer Elements anzupassen.</span><span class="sxs-lookup"><span data-stu-id="667fb-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="667fb-123">ShrinkToFit</span><span class="sxs-lookup"><span data-stu-id="667fb-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="667fb-124">Gibt einen Wert an, der angibt, ob das Video auf die für das Video Steuerelement definierte Breite und Höhe verkleinert wird, oder ruft diesen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="667fb-125">stretchdefit</span><span class="sxs-lookup"><span data-stu-id="667fb-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="667fb-126">Gibt einen Wert an, der angibt, ob sich das Video auf die für das Video Steuerelement definierte Breite und Höhe erstreckt, oder ruft diesen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="667fb-127">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="667fb-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="667fb-128">Gibt den QuickInfo-Text für das Videofenster an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="667fb-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="667fb-129">Windowless</span><span class="sxs-lookup"><span data-stu-id="667fb-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="667fb-130">Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob das Video Steuerelement Fenster oder Windows-los ist. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann.</span><span class="sxs-lookup"><span data-stu-id="667fb-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="667fb-131">Kann nur zur Entwurfszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="667fb-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="667fb-132">Skala</span><span class="sxs-lookup"><span data-stu-id="667fb-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="667fb-133">Gibt den Prozentsatz an, um den das Video skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="667fb-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="667fb-134">Das **Video** -Element kann die folgenden Ereignishandler implementieren.</span><span class="sxs-lookup"><span data-stu-id="667fb-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="667fb-135">Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="667fb-135">Event handler</span></span>                          | <span data-ttu-id="667fb-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="667fb-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="667fb-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="667fb-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="667fb-138">Behandelt ein Ereignis, das auftritt, wenn das Video das Rendering beendet und entladen wird.</span><span class="sxs-lookup"><span data-stu-id="667fb-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="667fb-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="667fb-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="667fb-140">Behandelt ein Ereignis, das auftritt, wenn das Video geladen und mit dem Rendering beginnt.</span><span class="sxs-lookup"><span data-stu-id="667fb-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="667fb-141">Das **Video** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren, sofern nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="667fb-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="667fb-142">Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="667fb-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="667fb-143">Vordefinierte Video Elemente sind normale **Video** Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="667fb-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="667fb-144">Die folgenden vordefinierten Video Elemente sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="667fb-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="667fb-145">Vordefiniertes Video</span><span class="sxs-lookup"><span data-stu-id="667fb-145">Predefined VIDEO</span></span>         | <span data-ttu-id="667fb-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="667fb-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="667fb-147">Wmpvideo</span><span class="sxs-lookup"><span data-stu-id="667fb-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="667fb-148">Ein **Video** Element, das das Video beim Ändern der Größe ausdehnt.</span><span class="sxs-lookup"><span data-stu-id="667fb-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="667fb-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="667fb-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="667fb-150">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="667fb-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




