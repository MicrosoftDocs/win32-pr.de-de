---
description: 'InkDisp-Klasse: Stellt die gesammelten Freihandstriche innerhalb eines Freihandraums dar.'
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109988"
---
# <a name="inkdisp-class"></a><span data-ttu-id="2a80b-103">InkDisp-Klasse</span><span class="sxs-lookup"><span data-stu-id="2a80b-103">InkDisp class</span></span>

<span data-ttu-id="2a80b-104">Stellt die gesammelten Freihandstriche innerhalb eines Freihandraums dar.</span><span class="sxs-lookup"><span data-stu-id="2a80b-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="2a80b-105">**InkDisp** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a80b-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="2a80b-106">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2a80b-106">Events</span></span>](#events)
-   [<span data-ttu-id="2a80b-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a80b-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="2a80b-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="2a80b-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="2a80b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a80b-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="2a80b-110">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2a80b-110">Events</span></span>

<span data-ttu-id="2a80b-111">Die **InkDisp-Klasse** verfügt über diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="2a80b-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="2a80b-112">Ereignis</span><span class="sxs-lookup"><span data-stu-id="2a80b-112">Event</span></span>                                    | <span data-ttu-id="2a80b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a80b-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="2a80b-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="2a80b-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="2a80b-115">Tritt ein, wenn dem **InkDisp-Objekt** ein Strich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2a80b-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="2a80b-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="2a80b-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="2a80b-117">Tritt ein, wenn ein Strich aus dem **InkDisp-Objekt** gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2a80b-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="2a80b-118">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a80b-118">Interfaces</span></span>

<span data-ttu-id="2a80b-119">Diese Schnittstellen werden von der **InkDisp-Klasse** definiert.</span><span class="sxs-lookup"><span data-stu-id="2a80b-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="2a80b-120">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2a80b-120">Interface</span></span>    | <span data-ttu-id="2a80b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a80b-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="2a80b-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="2a80b-122">**IInkDisp**</span></span> | <span data-ttu-id="2a80b-123">Dieses Objekt implementiert die **IInkDisp-COM-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="2a80b-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="2a80b-124">Methods</span></span>

<span data-ttu-id="2a80b-125">Die **InkDisp-Klasse** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2a80b-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="2a80b-126">Methode</span><span class="sxs-lookup"><span data-stu-id="2a80b-126">Method</span></span>                                                                   | <span data-ttu-id="2a80b-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a80b-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a80b-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="2a80b-129">Fügt eine Strichauflistung am angegebenen Rechteck in das **InkDisp-Objekt** ein.</span><span class="sxs-lookup"><span data-stu-id="2a80b-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2a80b-130">**Canpaste**</span><span class="sxs-lookup"><span data-stu-id="2a80b-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="2a80b-131">Gibt an, ob das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) in ein **InkDisp-Objekt** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a80b-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2a80b-132">**Clip**</span><span class="sxs-lookup"><span data-stu-id="2a80b-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="2a80b-133">Entfernt Teile eines Strichs oder eine Auflistung von Strichen, die sich außerhalb eines Rechtecks befinden.</span><span class="sxs-lookup"><span data-stu-id="2a80b-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2a80b-134">**Clipboardcopy**</span><span class="sxs-lookup"><span data-stu-id="2a80b-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="2a80b-135">Kopiert die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="2a80b-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="2a80b-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="2a80b-137">Kopiert die [**IInkStrokeDisp-Objekte,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) die im bekannten Rechteck enthalten sind, in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="2a80b-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="2a80b-138">**ZwischenablagePaste**</span><span class="sxs-lookup"><span data-stu-id="2a80b-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="2a80b-139">Kopiert das [**IDataObject aus**](/windows/desktop/api/objidl/nn-objidl-idataobject) der Zwischenablage in das **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2a80b-140">**Klon**</span><span class="sxs-lookup"><span data-stu-id="2a80b-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="2a80b-141">Erstellt ein doppeltes **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="2a80b-142">**Ink.createstroke**</span><span class="sxs-lookup"><span data-stu-id="2a80b-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="2a80b-143">Erstellt einen Strich aus Punkten oder Paketdaten.</span><span class="sxs-lookup"><span data-stu-id="2a80b-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="2a80b-144">**CreateStrokes**</span><span class="sxs-lookup"><span data-stu-id="2a80b-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="2a80b-145">Erstellt eine [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) für dieses **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="2a80b-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="2a80b-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="2a80b-147">Löscht einen Strich aus dem **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="2a80b-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="2a80b-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="2a80b-149">Löscht Striche aus dem **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="2a80b-150">**ExtractStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="2a80b-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="2a80b-151">Extrahiert Striche aus dem **InkDisp-Objekt** und gibt ein neues **InkDisp-Objekt** zurück, das die extrahierten Striche enthält.</span><span class="sxs-lookup"><span data-stu-id="2a80b-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="2a80b-152">**ExtractWithRectangle-Methode**</span><span class="sxs-lookup"><span data-stu-id="2a80b-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="2a80b-153">Striche aus einem vorhandenen **InkDisp-Klassenobjekt** werden schneidet oder kopiert und in ein neues Objekt der **InkDisp-Klasse** kopiert, indem das bekannte Rechteck verwendet wird, um zu bestimmen, welche Striche extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a80b-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="2a80b-154">**Getboundingbox**</span><span class="sxs-lookup"><span data-stu-id="2a80b-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="2a80b-155">Ruft das umgebende Feld aller Striche im **InkDisp-Objekt** ab.</span><span class="sxs-lookup"><span data-stu-id="2a80b-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="2a80b-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="2a80b-157">Ruft die [**InkStrokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die sich entweder vollständig innerhalb eines bekannten Kreises befindet oder von diesem schneidet.</span><span class="sxs-lookup"><span data-stu-id="2a80b-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="2a80b-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="2a80b-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="2a80b-159">Ruft die Striche innerhalb eines Polylinienauswahlbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="2a80b-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="2a80b-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="2a80b-161">Ruft die Striche ab, die in einem angegebenen Rechteck enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2a80b-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="2a80b-162">**Laden**</span><span class="sxs-lookup"><span data-stu-id="2a80b-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="2a80b-163">Füllt ein neues **InkDisp-Objekt** mit bekannten Binärdaten auf.</span><span class="sxs-lookup"><span data-stu-id="2a80b-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2a80b-164">**Ink.nearestpoint**</span><span class="sxs-lookup"><span data-stu-id="2a80b-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="2a80b-165">Ruft das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) innerhalb des **InkDisp-Objekts** ab, das einem bekannten Punkt am nächsten ist, und stellt optional zusätzliche Informationen bereit.</span><span class="sxs-lookup"><span data-stu-id="2a80b-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="2a80b-166">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="2a80b-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="2a80b-167">Konvertiert die Ink in ein angegebenes Format und gibt die Binärdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="2a80b-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="2a80b-168">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a80b-168">Properties</span></span>

<span data-ttu-id="2a80b-169">Die **InkDisp-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a80b-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="2a80b-170">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a80b-170">Property</span></span>                                                                           | <span data-ttu-id="2a80b-171">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2a80b-171">Access type</span></span>           | <span data-ttu-id="2a80b-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a80b-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a80b-173">**Customstrokes**</span><span class="sxs-lookup"><span data-stu-id="2a80b-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="2a80b-174">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a80b-174">Read-only</span></span><br/>  | <span data-ttu-id="2a80b-175">Ruft die [**IInkCustomStrokes-Auflistung**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) ab, die mit der Freihandeingabe beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a80b-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="2a80b-176">**Schmutzig**</span><span class="sxs-lookup"><span data-stu-id="2a80b-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="2a80b-177">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a80b-177">Read/write</span></span><br/> | <span data-ttu-id="2a80b-178">Ruft den Wert ab, der angibt, ob ein **InkDisp-Objekt** seit dem letzten Speichern der Ink geändert wurde, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="2a80b-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="2a80b-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="2a80b-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="2a80b-180">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a80b-180">Read-only</span></span><br/>  | <span data-ttu-id="2a80b-181">Ruft die Auflistung anwendungsdefinierter Daten ab.</span><span class="sxs-lookup"><span data-stu-id="2a80b-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="2a80b-182">**Striche**</span><span class="sxs-lookup"><span data-stu-id="2a80b-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="2a80b-183">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a80b-183">Read-only</span></span><br/>  | <span data-ttu-id="2a80b-184">Ruft die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ab, die im **InkDisp-Objekt** enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2a80b-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="2a80b-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a80b-185">Remarks</span></span>

<span data-ttu-id="2a80b-186">Dieses Objekt kann instanziiert werden, indem die [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2a80b-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="2a80b-187">Die erste Instanziierung dieses Objekts bewirkt, dass auch GDI+ instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a80b-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="2a80b-188">Ein Nebeneffekt ist, dass GDI+ immer wieder instanziiert wird, wenn Sie ein einzelnes Ink-Objekt in einer Schleife verwenden und es innerhalb der Schleife erstellen und zerstören.</span><span class="sxs-lookup"><span data-stu-id="2a80b-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="2a80b-189">Dies kann zu einer Leistungsbeeinträchtigung in Ihrer Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="2a80b-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="2a80b-190">Um dies zu verhindern, behalten Sie jederzeit eine einzelne Instanz eines Ink-Objekts bei, während Ihre Anwendung Ink verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a80b-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="2a80b-191">Ein **InkDisp-Objekt** ist ein Container mit Strichdaten (Punktdaten).</span><span class="sxs-lookup"><span data-stu-id="2a80b-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="2a80b-192">Die Strichdaten oder die vom Stift gesammelten Punkte werden in ein **InkDisp-Objekt** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2a80b-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="2a80b-193">Die [**Strokes-Eigenschaft**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) enthält die Daten für alle Striche innerhalb des **InkDisp-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="2a80b-194">Das [**InkCollector-Objekt,**](inkcollector-class.md) [**das InkOverlay-Objekt**](inkoverlay-class.md) und das [InkPicture-Steuerelement](inkpicture-control-reference.md) sammeln Punkte vom Eingabegerät und speichern sie in einem **InkDisp-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="2a80b-195">Diese Objekte fungieren im Wesentlichen als Quelle, die Ink an ein oder viele verschiedene **InkDisp-Objekte** verteilt, die als Container fungieren, die die verteilte Ink-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="2a80b-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="2a80b-196">Der Freiraum ist ein virtueller Koordinatenraum, dem die Koordinaten des Tablet-Kontexts zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2a80b-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="2a80b-197">Dieses Leerzeichen ist auf ein HIMETRIC-Koordinatensystem festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2a80b-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="2a80b-198">In Freiraumkoordinaten entspricht eine Bewegung von 0 zu 1 1 HIMETRIC-Einheit.</span><span class="sxs-lookup"><span data-stu-id="2a80b-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="2a80b-199">Diese Zuordnung erleichtert das Zuordnen mehrerer **InkDisp-Objekte.**</span><span class="sxs-lookup"><span data-stu-id="2a80b-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="2a80b-200">Das [**InkRenderer-Objekt**](inkrenderer-class.md) verwaltet die Zuordnungen zwischen Ink und dem Anzeigefenster.</span><span class="sxs-lookup"><span data-stu-id="2a80b-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a80b-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a80b-201">Requirements</span></span>



| <span data-ttu-id="2a80b-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a80b-202">Requirement</span></span> | <span data-ttu-id="2a80b-203">Wert</span><span class="sxs-lookup"><span data-stu-id="2a80b-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a80b-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a80b-204">Minimum supported client</span></span><br/> | <span data-ttu-id="2a80b-205">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="2a80b-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2a80b-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a80b-206">Minimum supported server</span></span><br/> | <span data-ttu-id="2a80b-207">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2a80b-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2a80b-208">Header</span><span class="sxs-lookup"><span data-stu-id="2a80b-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a80b-209"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="2a80b-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2a80b-210">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a80b-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a80b-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a80b-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2a80b-212">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2a80b-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a80b-213">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="2a80b-214">[InkStrokes-Sammlung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a80b-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2a80b-215">**IInkTablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2a80b-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

