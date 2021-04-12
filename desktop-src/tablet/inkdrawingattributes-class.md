---
description: Stellt die Attribute dar, die beim Zeichnen auf frei Hand Eingaben angewendet werden.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Inkdrawingattributes-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347908"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="61640-103">Inkdrawingattributes-Klasse</span><span class="sxs-lookup"><span data-stu-id="61640-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="61640-104">Stellt die Attribute dar, die beim Zeichnen auf frei Hand Eingaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="61640-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="61640-105">**Inkdrawingattributes** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="61640-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="61640-106">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="61640-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="61640-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="61640-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="61640-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61640-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="61640-109">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="61640-109">Interfaces</span></span>

<span data-ttu-id="61640-110">Diese Schnittstellen werden von der **inkdrawingattributes** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="61640-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="61640-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="61640-111">Interface</span></span>                 | <span data-ttu-id="61640-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61640-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="61640-113">**Iinkdrawingattributes**</span><span class="sxs-lookup"><span data-stu-id="61640-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="61640-114">Dieses Objekt implementiert die **iinkdrawingattributes** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="61640-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="61640-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="61640-115">Methods</span></span>

<span data-ttu-id="61640-116">Die **inkdrawingattributes** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="61640-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="61640-117">Methode</span><span class="sxs-lookup"><span data-stu-id="61640-117">Method</span></span>                         | <span data-ttu-id="61640-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61640-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61640-119">**Klon**</span><span class="sxs-lookup"><span data-stu-id="61640-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="61640-120">Erstellt ein doppeltes [**InkDisp**](inkdisp-class.md)-, **inkdrawingattributes**-oder [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="61640-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="61640-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61640-121">Properties</span></span>

<span data-ttu-id="61640-122">Die **inkdrawingattributes** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61640-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="61640-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61640-123">Property</span></span>                                                                           | <span data-ttu-id="61640-124">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="61640-124">Access type</span></span>           | <span data-ttu-id="61640-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61640-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61640-126">**Geglättet**</span><span class="sxs-lookup"><span data-stu-id="61640-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="61640-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-127">Read/write</span></span><br/> | <span data-ttu-id="61640-128">Ruft den-Wert ab, der angibt, ob die Vordergrund-und Hintergrundfarben entlang der Kante des frei Hand Zeigern gemischt werden, um die Glätte eines frei Hand Strichs zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="61640-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="61640-129">**Color**</span><span class="sxs-lookup"><span data-stu-id="61640-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="61640-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-130">Read/write</span></span><br/> | <span data-ttu-id="61640-131">Ruft die Farbe der mit diesem **inkdrawingattributes** -Objekt gezeichneten frei Handschrift ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="61640-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="61640-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="61640-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="61640-133">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="61640-133">Read-only</span></span><br/>  | <span data-ttu-id="61640-134">Ruft die Auflistung von Anwendungs definierten Daten ab, die im **inkdrawingattributes** -Objekt gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="61640-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="61640-135">**Fitum Curve**</span><span class="sxs-lookup"><span data-stu-id="61640-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="61640-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-136">Read/write</span></span><br/> | <span data-ttu-id="61640-137">Ruft den-Wert ab, der angibt, ob frei Hand Eingaben als eine Reihe von Kurven anstelle von Linien zwischen Stift-Stichprobenpunkten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="61640-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="61640-138">**Höhe**</span><span class="sxs-lookup"><span data-stu-id="61640-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="61640-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-139">Read/write</span></span><br/> | <span data-ttu-id="61640-140">Ruft die Höhe des Stifts beim Zeichnen von frei Hand Eingaben mit diesem **inkdrawingattributes** -Objekt ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="61640-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="61640-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="61640-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="61640-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-142">Read/write</span></span><br/> | <span data-ttu-id="61640-143">Ruft den Wert ab oder legt ihn fest, der angibt, ob das Zeichnen von frei Hand Eingaben mit erhöhtem Druck der Stift Spitze auf der Tablet-Oberfläche breiter wird.</span><span class="sxs-lookup"><span data-stu-id="61640-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="61640-144">**Trinkgeld**</span><span class="sxs-lookup"><span data-stu-id="61640-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="61640-145">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-145">Read/write</span></span><br/> | <span data-ttu-id="61640-146">Ruft den zu verwendenden Stift Tipp (Ball oder Rechteck) beim Zeichnen von frei Hand Eingaben mit diesem **inkdrawingattributes** -Objekt ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="61640-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="61640-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="61640-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="61640-148">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-148">Read/write</span></span><br/> | <span data-ttu-id="61640-149">Ruft ab oder legt fest, wie die Stift Farbe mit den vorhandenen Hintergrundfarben auf der Anzeige interagiert, wenn die frei Hand Eingaben gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="61640-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="61640-150">**Transparenz**</span><span class="sxs-lookup"><span data-stu-id="61640-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="61640-151">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-151">Read/write</span></span><br/> | <span data-ttu-id="61640-152">Ruft den Transparenz Wert der gezeichneten frei Hand Eingabe ab oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="61640-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="61640-153">Die Werte reichen von 0 (null) bis 255 (vollständig transparent).</span><span class="sxs-lookup"><span data-stu-id="61640-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="61640-154">**Breite**</span><span class="sxs-lookup"><span data-stu-id="61640-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="61640-155">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="61640-155">Read/write</span></span><br/> | <span data-ttu-id="61640-156">Ruft die Breite des Stifts beim Zeichnen von Ink mit diesem **inkdrawingattributes** -Objekt ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="61640-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="61640-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61640-157">Remarks</span></span>

<span data-ttu-id="61640-158">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="61640-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="61640-159">Diese Zeichnungs Attribute können einem Strich oder Cursor zugeordnet werden und legen Einstellungen wie Farbe, Breite und Transparenz fest.</span><span class="sxs-lookup"><span data-stu-id="61640-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="61640-160">Um die Zeichnungs Attribute eines Strichs anzugeben, verwenden Sie die [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) -Eigenschaft des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="61640-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="61640-161">Um die Zeichnungs Attribute aller Striche innerhalb einer Auflistung von Strichen anzugeben, nennen Sie die [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) -Methode der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="61640-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="61640-162">Jedes [**InkCollector**](inkcollector-class.md) -Objekt, [**InkOverlay**](inkoverlay-class.md) -Objekt und [InkPicture](inkpicture-control-reference.md) -Steuerelement können einen anderen Satz von Zeichnungs Attributen für denselben Cursor angeben.</span><span class="sxs-lookup"><span data-stu-id="61640-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="61640-163">Verwenden Sie die [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) -Eigenschaft des [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekts, um die Zeichnungs Attribute eines Cursors zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="61640-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="61640-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61640-164">Requirements</span></span>



| <span data-ttu-id="61640-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61640-165">Requirement</span></span> | <span data-ttu-id="61640-166">Wert</span><span class="sxs-lookup"><span data-stu-id="61640-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61640-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61640-167">Minimum supported client</span></span><br/> | <span data-ttu-id="61640-168">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61640-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="61640-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61640-169">Minimum supported server</span></span><br/> | <span data-ttu-id="61640-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61640-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="61640-171">Header</span><span class="sxs-lookup"><span data-stu-id="61640-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="61640-172"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="61640-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="61640-173">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="61640-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="61640-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61640-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="61640-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61640-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61640-176">**DrawingAttributes-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="61640-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="61640-177">**DrawingAttributes-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="61640-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="61640-178">**DrawingAttributes-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="61640-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="61640-179">**DefaultDrawingAttributes (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="61640-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="61640-180">**DefaultDrawingAttributes (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="61640-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="61640-181">**DefaultDrawingAttributes (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="61640-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="61640-182">**ModifyDrawingAttributes-Methode**</span><span class="sxs-lookup"><span data-stu-id="61640-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="61640-183">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="61640-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="61640-184">**InkDisp-Klasse**</span><span class="sxs-lookup"><span data-stu-id="61640-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="61640-185">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="61640-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

