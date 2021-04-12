---
description: Stellt die Verwaltung von Zuordnungen von frei Hand Eingaben zum Anzeige Fenster dar. Verwenden Sie das inkrenderer-Objekt, um frei Hand Eingaben in einem Fenster anzuzeigen. Sie können es auch zum Neupositionieren und Ändern der Größe des Strichs verwenden.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Inkrenderer-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218577"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="e0305-105">Inkrenderer-Klasse</span><span class="sxs-lookup"><span data-stu-id="e0305-105">InkRenderer class</span></span>

<span data-ttu-id="e0305-106">Stellt die Verwaltung von Zuordnungen von frei Hand Eingaben zum Anzeige Fenster dar.</span><span class="sxs-lookup"><span data-stu-id="e0305-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="e0305-107">Verwenden Sie das **inkrenderer** -Objekt, um frei Hand Eingaben in einem Fenster anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e0305-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="e0305-108">Sie können es auch zum Neupositionieren und Ändern der Größe des Strichs verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0305-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="e0305-109">Der **inkrenderer** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e0305-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="e0305-110">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e0305-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="e0305-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="e0305-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="e0305-112">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e0305-112">Interfaces</span></span>

<span data-ttu-id="e0305-113">Diese Schnittstellen werden von der **inkrenderer** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="e0305-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="e0305-114">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e0305-114">Interface</span></span>        | <span data-ttu-id="e0305-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0305-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="e0305-116">**Iinkrenderer**</span><span class="sxs-lookup"><span data-stu-id="e0305-116">**IInkRenderer**</span></span> | <span data-ttu-id="e0305-117">Dieses Objekt implementiert die **iinkrenderer** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0305-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="e0305-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="e0305-118">Methods</span></span>

<span data-ttu-id="e0305-119">Die **inkrenderer** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e0305-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="e0305-120">Methode</span><span class="sxs-lookup"><span data-stu-id="e0305-120">Method</span></span>                                                                     | <span data-ttu-id="e0305-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0305-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0305-122">**Draw**</span><span class="sxs-lookup"><span data-stu-id="e0305-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="e0305-123">Zeichnet Striche in einem Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="e0305-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e0305-124">**Drawstroke**</span><span class="sxs-lookup"><span data-stu-id="e0305-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="e0305-125">Zeichnet einen Strich im angegebenen Windows-Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="e0305-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e0305-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="e0305-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="e0305-127">Ruft die Objekt Transformation ab, die zum RenderInk verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e0305-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="e0305-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="e0305-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="e0305-129">Ruft die Ansichts Transformation ab, die zum RenderInk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0305-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="e0305-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="e0305-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="e0305-131">Konvertiert einen Speicherort in frei Hand Raumkoordinaten in Pixel Raum.</span><span class="sxs-lookup"><span data-stu-id="e0305-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="e0305-132">**Inkspacetopixelfrompoints**</span><span class="sxs-lookup"><span data-stu-id="e0305-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="e0305-133">Konvertiert ein Array von Punkten in frei Hand Raumkoordinaten in den Pixel Raum.</span><span class="sxs-lookup"><span data-stu-id="e0305-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="e0305-134">**Measure**</span><span class="sxs-lookup"><span data-stu-id="e0305-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="e0305-135">Berechnet das Rechteck im Gerätekontext, das eine Auflistung von Strichen enthalten würde, wenn Sie mit dem **inkrenderer** -Objekt gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e0305-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="e0305-136">**Messrestroke**</span><span class="sxs-lookup"><span data-stu-id="e0305-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="e0305-137">Berechnet das Rechteck im Gerätekontext, das einen Strich enthalten würde, wenn Sie mit dem **inkrenderer** -Objekt gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e0305-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="e0305-138">**Move**</span><span class="sxs-lookup"><span data-stu-id="e0305-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="e0305-139">Wendet eine Übersetzung auf die Ansichts Transformation in Freihand Raumkoordinaten an.</span><span class="sxs-lookup"><span data-stu-id="e0305-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="e0305-140">**Pixelesinkspace**</span><span class="sxs-lookup"><span data-stu-id="e0305-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="e0305-141">Konvertiert einen Speicherort in Pixelkoordinaten in den frei Handbereich.</span><span class="sxs-lookup"><span data-stu-id="e0305-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e0305-142">**Pixelroinkspacefrompoints**</span><span class="sxs-lookup"><span data-stu-id="e0305-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="e0305-143">Konvertiert ein Array von Punkten in Pixel Raumkoordinaten in frei Hand Raum.</span><span class="sxs-lookup"><span data-stu-id="e0305-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="e0305-144">**Drehen**</span><span class="sxs-lookup"><span data-stu-id="e0305-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="e0305-145">Wendet eine Drehung auf die Ansichts Transformation an.</span><span class="sxs-lookup"><span data-stu-id="e0305-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="e0305-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="e0305-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="e0305-147">Skaliert die Ansichts Transformation in der X-und Y-Dimension.</span><span class="sxs-lookup"><span data-stu-id="e0305-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e0305-148">**"Stobjecttransform"**</span><span class="sxs-lookup"><span data-stu-id="e0305-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="e0305-149">Legt die Objekt Transformation fest, die zum RenderInk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0305-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="e0305-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="e0305-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="e0305-151">Legt die Ansichts Transformation fest, die zum RenderInk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0305-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="e0305-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0305-152">Remarks</span></span>

<span data-ttu-id="e0305-153">Der Druckvorgang wird auch über das **inkrenderer** -Objekt durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0305-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="e0305-154">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0305-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0305-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0305-155">Requirements</span></span>



| <span data-ttu-id="e0305-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0305-156">Requirement</span></span> | <span data-ttu-id="e0305-157">Wert</span><span class="sxs-lookup"><span data-stu-id="e0305-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0305-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0305-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e0305-159">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0305-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e0305-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0305-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e0305-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e0305-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e0305-162">Header</span><span class="sxs-lookup"><span data-stu-id="e0305-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0305-163"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e0305-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e0305-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0305-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0305-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0305-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e0305-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0305-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0305-167">**Renderer (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="e0305-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="e0305-168">**Inkdrawingattributes-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e0305-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="e0305-169">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e0305-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="e0305-170">[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0305-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

