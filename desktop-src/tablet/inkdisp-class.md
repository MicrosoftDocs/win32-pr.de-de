---
description: Stellt die gesammelten Hand Striche innerhalb eines frei Hand Raums dar.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: InkDisp-Klasse (msink AUT. h)
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
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750209"
---
# <a name="inkdisp-class"></a><span data-ttu-id="8af11-103">InkDisp-Klasse</span><span class="sxs-lookup"><span data-stu-id="8af11-103">InkDisp class</span></span>

<span data-ttu-id="8af11-104">Stellt die gesammelten Hand Striche innerhalb eines frei Hand Raums dar.</span><span class="sxs-lookup"><span data-stu-id="8af11-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="8af11-105">**InkDisp** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8af11-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="8af11-106">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8af11-106">Events</span></span>](#events)
-   [<span data-ttu-id="8af11-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8af11-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="8af11-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8af11-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="8af11-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8af11-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="8af11-110">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8af11-110">Events</span></span>

<span data-ttu-id="8af11-111">Die **InkDisp** -Klasse enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8af11-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="8af11-112">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8af11-112">Event</span></span>                                    | <span data-ttu-id="8af11-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8af11-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="8af11-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="8af11-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="8af11-115">Tritt auf, wenn dem **InkDisp** -Objekt ein Strich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8af11-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="8af11-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="8af11-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="8af11-117">Tritt auf, wenn ein Strich aus dem **InkDisp** -Objekt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="8af11-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="8af11-118">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8af11-118">Interfaces</span></span>

<span data-ttu-id="8af11-119">Diese Schnittstellen werden von der **InkDisp** -Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="8af11-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="8af11-120">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8af11-120">Interface</span></span>    | <span data-ttu-id="8af11-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8af11-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="8af11-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="8af11-122">**IInkDisp**</span></span> | <span data-ttu-id="8af11-123">Dieses Objekt implementiert die **IInkDisp** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8af11-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="8af11-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="8af11-124">Methods</span></span>

<span data-ttu-id="8af11-125">Die **InkDisp** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8af11-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="8af11-126">Methode</span><span class="sxs-lookup"><span data-stu-id="8af11-126">Method</span></span>                                                                   | <span data-ttu-id="8af11-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8af11-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8af11-128">**Addstrokesatrechteck**</span><span class="sxs-lookup"><span data-stu-id="8af11-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="8af11-129">Fügt eine Strich Auflistung im angegebenen Rechteck in das **InkDisp** -Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="8af11-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8af11-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="8af11-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="8af11-131">Gibt an, ob das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) -Objekt in ein **InkDisp** -Objekt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8af11-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="8af11-132">**Techno**</span><span class="sxs-lookup"><span data-stu-id="8af11-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="8af11-133">Entfernt Teile eines Strichs oder eine Auflistung von Strichen außerhalb eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8af11-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8af11-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="8af11-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="8af11-135">Kopiert die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="8af11-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="8af11-136">**Clipboardcopywithrechteck**</span><span class="sxs-lookup"><span data-stu-id="8af11-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="8af11-137">Kopiert die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte, die im bekannten Rechteck enthalten sind, in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="8af11-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="8af11-138">**ClipboardPaste**</span><span class="sxs-lookup"><span data-stu-id="8af11-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="8af11-139">Kopiert das [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) aus der Zwischenablage in das **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="8af11-140">**Klon**</span><span class="sxs-lookup"><span data-stu-id="8af11-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="8af11-141">Erstellt ein doppeltes **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="8af11-142">**"Kreatestroke"**</span><span class="sxs-lookup"><span data-stu-id="8af11-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="8af11-143">Erstellt einen Strich aus Punkten oder Paketdaten.</span><span class="sxs-lookup"><span data-stu-id="8af11-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="8af11-144">**"Kreatestrokes"**</span><span class="sxs-lookup"><span data-stu-id="8af11-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="8af11-145">Erstellt eine [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung für dieses **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="8af11-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="8af11-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="8af11-147">Löscht einen Strich aus dem **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="8af11-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="8af11-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="8af11-149">Löscht Striche aus dem **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="8af11-150">**ExtractStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="8af11-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="8af11-151">Extrahiert Striche aus dem **InkDisp** -Objekt und gibt ein neues **InkDisp** -Objekt zurück, das die extrahierten Striche enthält.</span><span class="sxs-lookup"><span data-stu-id="8af11-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="8af11-152">**Extractwithrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="8af11-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="8af11-153">Schneidet Striche von einem vorhandenen InkDisp- **Klassen** Objekt ab oder kopiert sie in ein neues **InkDisp-Klassen** Objekt, indem das bekannte Rechteck verwendet wird, um zu bestimmen, welche Striche extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8af11-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="8af11-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="8af11-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="8af11-155">Ruft das umgebende Feld aller Striche im **InkDisp** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="8af11-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="8af11-156">**Hittestcircle**</span><span class="sxs-lookup"><span data-stu-id="8af11-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="8af11-157">Ruft die [**inkstrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab, die sich entweder vollständig innerhalb oder durch einen Bekanntenkreis überschneiden.</span><span class="sxs-lookup"><span data-stu-id="8af11-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="8af11-158">**Hittestwithlasso**</span><span class="sxs-lookup"><span data-stu-id="8af11-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="8af11-159">Ruft die Striche innerhalb eines polylinienauswahlbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="8af11-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="8af11-160">**Hittestwithrechteck**</span><span class="sxs-lookup"><span data-stu-id="8af11-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="8af11-161">Ruft die Striche ab, die innerhalb eines angegebenen Rechtecks enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8af11-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8af11-162">**Laden**</span><span class="sxs-lookup"><span data-stu-id="8af11-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="8af11-163">Füllt ein neues **InkDisp** -Objekt mit bekannten Binärdaten auf.</span><span class="sxs-lookup"><span data-stu-id="8af11-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="8af11-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="8af11-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="8af11-165">Ruft das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt im **InkDisp** -Objekt ab, das sich am nächsten an einem bekannten Punkt befindet, wobei optional zusätzliche Informationen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8af11-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="8af11-166">**Speichern**</span><span class="sxs-lookup"><span data-stu-id="8af11-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="8af11-167">Konvertiert die frei Hand Eingabe in ein angegebenes Format und gibt die Binärdaten zurück.</span><span class="sxs-lookup"><span data-stu-id="8af11-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="8af11-168">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8af11-168">Properties</span></span>

<span data-ttu-id="8af11-169">Die **InkDisp** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8af11-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="8af11-170">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8af11-170">Property</span></span>                                                                           | <span data-ttu-id="8af11-171">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8af11-171">Access type</span></span>           | <span data-ttu-id="8af11-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8af11-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8af11-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="8af11-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="8af11-174">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8af11-174">Read-only</span></span><br/>  | <span data-ttu-id="8af11-175">Ruft die [**iinkcustomstrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) -Auflistung ab, die mit der frei Hand Eingabe beibehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="8af11-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="8af11-176">**TZI**</span><span class="sxs-lookup"><span data-stu-id="8af11-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="8af11-177">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8af11-177">Read/write</span></span><br/> | <span data-ttu-id="8af11-178">Ruft den Wert ab, der angibt, ob ein **InkDisp** -Objekt seit dem letzten Speichern der frei Hand Eingabe geändert wurde, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="8af11-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="8af11-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="8af11-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="8af11-180">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8af11-180">Read-only</span></span><br/>  | <span data-ttu-id="8af11-181">Ruft die Auflistung von Anwendungs definierten Daten ab.</span><span class="sxs-lookup"><span data-stu-id="8af11-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="8af11-182">**Striche**</span><span class="sxs-lookup"><span data-stu-id="8af11-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="8af11-183">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8af11-183">Read-only</span></span><br/>  | <span data-ttu-id="8af11-184">Ruft die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ab, die im **InkDisp** -Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8af11-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="8af11-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8af11-185">Remarks</span></span>

<span data-ttu-id="8af11-186">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="8af11-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="8af11-187">Die erste Instanziierung dieses Objekts bewirkt, dass GDI+ ebenfalls instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="8af11-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="8af11-188">Ein Nebeneffekt ist, dass bei Verwendung eines einzelnen frei Hand Objekts in einer Schleife, das in der Schleife erstellt und zerstört wird, GDI+ immer wieder instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="8af11-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="8af11-189">Dies kann zu Leistungseinbußen in Ihrer Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="8af11-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="8af11-190">Um dies zu verhindern, behalten Sie immer eine einzelne Instanz eines Ink-Objekts bei, während Ihre Anwendung frei Hand Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="8af11-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="8af11-191">Ein **InkDisp** -Objekt ist ein Container von Stroke-Daten (Point).</span><span class="sxs-lookup"><span data-stu-id="8af11-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="8af11-192">Die Strich Daten oder die vom Stift erfassten Punkte werden in ein **InkDisp** -Objekt eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8af11-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="8af11-193">Die [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) -Eigenschaft enthält die Daten für alle Striche innerhalb des **InkDisp** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="8af11-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="8af11-194">Das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt und das [InkPicture](inkpicture-control-reference.md) -Steuerelement sammelt Punkte vom Eingabegerät und setzt Sie in ein **InkDisp** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8af11-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="8af11-195">Diese Objekte fungieren im Wesentlichen als Quelle, die frei Hand Eingaben an ein oder mehrere verschiedene **InkDisp** -Objekte verteilt, die als Container fungieren, die den verteilten frei Hand Eingaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="8af11-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="8af11-196">Der frei Hand Raum ist ein virtueller Koordinaten Bereich, dem die Koordinaten des Tablet-Kontexts zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8af11-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="8af11-197">Dieser Raum ist auf ein HIMETRIC-Koordinatensystem korrigiert.</span><span class="sxs-lookup"><span data-stu-id="8af11-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="8af11-198">In frei Hand Raumkoordinaten ist ein Wechsel zwischen 0 und 1 ein Wert von 1 himetrik.</span><span class="sxs-lookup"><span data-stu-id="8af11-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="8af11-199">Mit dieser Zuordnung können mehrere **InkDisp** -Objekte problemlos miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="8af11-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="8af11-200">Das [**inkrenderer**](inkrenderer-class.md) -Objekt verwaltet die Zuordnungen zwischen frei Hand Eingaben und dem Anzeige Fenster.</span><span class="sxs-lookup"><span data-stu-id="8af11-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af11-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8af11-201">Requirements</span></span>



| <span data-ttu-id="8af11-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8af11-202">Requirement</span></span> | <span data-ttu-id="8af11-203">Wert</span><span class="sxs-lookup"><span data-stu-id="8af11-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af11-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8af11-204">Minimum supported client</span></span><br/> | <span data-ttu-id="8af11-205">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8af11-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8af11-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8af11-206">Minimum supported server</span></span><br/> | <span data-ttu-id="8af11-207">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8af11-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8af11-208">Header</span><span class="sxs-lookup"><span data-stu-id="8af11-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af11-209"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8af11-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8af11-210">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8af11-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="8af11-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8af11-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8af11-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8af11-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af11-213">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8af11-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="8af11-214">[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8af11-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8af11-215">**Iinktablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8af11-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

