---
title: Iwmpmedia (VB und C)-Schnittstelle (WMP. h)
description: Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medien Elements. Die iwmpmedia-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Iwmpmedia (VB und C) Interface Windows Media Player
- Iwmpmedia (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367749"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="2dddf-105">Iwmpmedia (VB und c#)-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2dddf-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="2dddf-106">Bietet eine Möglichkeit zum Festlegen und Abrufen der Eigenschaften eines Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="2dddf-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="2dddf-107">Die **iwmpmedia** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2dddf-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="2dddf-108">Member</span><span class="sxs-lookup"><span data-stu-id="2dddf-108">Members</span></span>

<span data-ttu-id="2dddf-109">Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2dddf-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="2dddf-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="2dddf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2dddf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2dddf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2dddf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2dddf-112">Methods</span></span>

<span data-ttu-id="2dddf-113">Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2dddf-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="2dddf-114">Methode</span><span class="sxs-lookup"><span data-stu-id="2dddf-114">Method</span></span>                                                                             | <span data-ttu-id="2dddf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dddf-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dddf-116">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="2dddf-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="2dddf-117">Gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="2dddf-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="2dddf-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2dddf-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="2dddf-119">Gibt den Wert des angegebenen Attributs für das Medien Element zurück.</span><span class="sxs-lookup"><span data-stu-id="2dddf-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="2dddf-120">**getiteminfobyatom**</span><span class="sxs-lookup"><span data-stu-id="2dddf-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="2dddf-121">Gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.</span><span class="sxs-lookup"><span data-stu-id="2dddf-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="2dddf-122">**getmarkername**</span><span class="sxs-lookup"><span data-stu-id="2dddf-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="2dddf-123">Gibt den Namen des Markers am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="2dddf-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="2dddf-124">**getmarkertime**</span><span class="sxs-lookup"><span data-stu-id="2dddf-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="2dddf-125">Gibt die Zeit des Markers am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="2dddf-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="2dddf-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="2dddf-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="2dddf-127">Gibt einen Wert zurück, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="2dddf-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="2dddf-128">**isread onlyitem**</span><span class="sxs-lookup"><span data-stu-id="2dddf-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="2dddf-129">Gibt einen Wert zurück, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="2dddf-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="2dddf-130">**"Einstellungs Element"**</span><span class="sxs-lookup"><span data-stu-id="2dddf-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="2dddf-131">Legt den Wert des angegebenen Attributs für das Medien Element fest.</span><span class="sxs-lookup"><span data-stu-id="2dddf-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="2dddf-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2dddf-132">Properties</span></span>

<span data-ttu-id="2dddf-133">Die **iwmpmedia-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2dddf-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="2dddf-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2dddf-134">Property</span></span>                                                                                      | <span data-ttu-id="2dddf-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2dddf-135">Access type</span></span>          | <span data-ttu-id="2dddf-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dddf-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dddf-137">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="2dddf-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="2dddf-138">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-138">Read-only</span></span><br/> | <span data-ttu-id="2dddf-139">Ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="2dddf-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="2dddf-140">**auf**</span><span class="sxs-lookup"><span data-stu-id="2dddf-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="2dddf-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-141">Read-only</span></span><br/> | <span data-ttu-id="2dddf-142">Ruft die Dauer des aktuellen Medien Elements in Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="2dddf-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="2dddf-143">**durationString**</span><span class="sxs-lookup"><span data-stu-id="2dddf-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="2dddf-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-144">Read-only</span></span><br/> | <span data-ttu-id="2dddf-145">Ruft einen Wert ab, der die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt.</span><span class="sxs-lookup"><span data-stu-id="2dddf-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="2dddf-146">**imagesourceheight**</span><span class="sxs-lookup"><span data-stu-id="2dddf-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="2dddf-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-147">Read-only</span></span><br/> | <span data-ttu-id="2dddf-148">Ruft die Höhe des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="2dddf-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="2dddf-149">**imagesourcewidth**</span><span class="sxs-lookup"><span data-stu-id="2dddf-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="2dddf-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-150">Read-only</span></span><br/> | <span data-ttu-id="2dddf-151">Ruft die Breite des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="2dddf-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2dddf-152">**isidentical**</span><span class="sxs-lookup"><span data-stu-id="2dddf-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="2dddf-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-153">Read-only</span></span><br/> | <span data-ttu-id="2dddf-154">Ruft einen Wert ab, der angibt, ob das angegebene Medien Element mit dem aktuellen Medien Element identisch ist.</span><span class="sxs-lookup"><span data-stu-id="2dddf-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="2dddf-155">In c# ist dies die **get \_ isidentical** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2dddf-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="2dddf-156">**markercount**</span><span class="sxs-lookup"><span data-stu-id="2dddf-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="2dddf-157">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-157">Read-only</span></span><br/> | <span data-ttu-id="2dddf-158">Ruft die Anzahl der Marker im Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="2dddf-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="2dddf-159">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="2dddf-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="2dddf-160">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-160">Read-only</span></span><br/> | <span data-ttu-id="2dddf-161">Ruft den Namen des Medien Elements ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="2dddf-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="2dddf-162">**SourceURL**</span><span class="sxs-lookup"><span data-stu-id="2dddf-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="2dddf-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2dddf-163">Read-only</span></span><br/> | <span data-ttu-id="2dddf-164">Ruft die URL des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="2dddf-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="2dddf-165">Abrufen einer **iwmpmedia** -Schnittstelle mithilfe der folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="2dddf-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="2dddf-166">Objekt oder Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2dddf-166">Object or interface</span></span>                                               | <span data-ttu-id="2dddf-167">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="2dddf-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2dddf-168">**Iwmpcontrols**</span><span class="sxs-lookup"><span data-stu-id="2dddf-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="2dddf-169">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="2dddf-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="2dddf-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="2dddf-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="2dddf-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newmedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="2dddf-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="2dddf-172">**Iwmpwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="2dddf-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="2dddf-173">[**Item**](iwmpplaylist-item--vb-and-c.md) ( \_ Element in c# Get)</span><span class="sxs-lookup"><span data-stu-id="2dddf-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="2dddf-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dddf-174">Requirements</span></span>



| <span data-ttu-id="2dddf-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dddf-175">Requirement</span></span> | <span data-ttu-id="2dddf-176">Wert</span><span class="sxs-lookup"><span data-stu-id="2dddf-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2dddf-177">Header</span><span class="sxs-lookup"><span data-stu-id="2dddf-177">Header</span></span><br/> | <dl> <span data-ttu-id="2dddf-178"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dddf-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dddf-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dddf-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dddf-180">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="2dddf-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="2dddf-181">**IWMPMedia2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2dddf-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2dddf-182">**IWMPMedia3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2dddf-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





