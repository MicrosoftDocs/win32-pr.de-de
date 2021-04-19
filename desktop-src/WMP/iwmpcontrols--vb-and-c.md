---
title: Iwmpcontrols (VB und C)-Schnittstelle (WMP. h)
description: Bietet eine Möglichkeit, die Wiedergabe eines Medien Elements zu manipulieren, indem die Transport Steuerelemente von Windows-Media Player dargestellt werden, z. b. wiedergeben, anhalten und anhalten. die iwmpcontrols-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Iwmpcontrols (VB und C) Interface Windows Media Player
- Iwmpcontrols (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373765"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="bab00-105">Iwmpcontrols (VB und c#)-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bab00-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="bab00-106">Bietet eine Möglichkeit, die Wiedergabe eines Medien Elements zu manipulieren, indem die Transport Steuerelemente von Windows-Media Player dargestellt werden, z. b. Wiedergabe, anhalten und anhalten.</span><span class="sxs-lookup"><span data-stu-id="bab00-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="bab00-107">Die **iwmpcontrols** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bab00-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="bab00-108">Member</span><span class="sxs-lookup"><span data-stu-id="bab00-108">Members</span></span>

<span data-ttu-id="bab00-109">Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bab00-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="bab00-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="bab00-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bab00-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bab00-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bab00-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="bab00-112">Methods</span></span>

<span data-ttu-id="bab00-113">Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bab00-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="bab00-114">Methode</span><span class="sxs-lookup"><span data-stu-id="bab00-114">Method</span></span>                                                                       | <span data-ttu-id="bab00-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bab00-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bab00-116">**FastForward**</span><span class="sxs-lookup"><span data-stu-id="bab00-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="bab00-117">Startet die schnelle Wiedergabe des Medien Elements in Vorwärtsrichtung.</span><span class="sxs-lookup"><span data-stu-id="bab00-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="bab00-118">**fastreverse**</span><span class="sxs-lookup"><span data-stu-id="bab00-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="bab00-119">Startet die schnelle Wiedergabe des Medien Elements in umgekehrter Richtung.</span><span class="sxs-lookup"><span data-stu-id="bab00-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="bab00-120">**weiter**</span><span class="sxs-lookup"><span data-stu-id="bab00-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="bab00-121">Legt das nächste Element in der Wiedergabeliste als Aktuelles Element fest.</span><span class="sxs-lookup"><span data-stu-id="bab00-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="bab00-122">**Brechung**</span><span class="sxs-lookup"><span data-stu-id="bab00-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="bab00-123">Hält die Wiedergabe des Medien Elements an.</span><span class="sxs-lookup"><span data-stu-id="bab00-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="bab00-124">**Theater**</span><span class="sxs-lookup"><span data-stu-id="bab00-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="bab00-125">Startet die Wiedergabe des aktuellen Medien Elements oder nimmt die Wiedergabe eines angehaltenen Elements wieder auf.</span><span class="sxs-lookup"><span data-stu-id="bab00-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="bab00-126">**PlayItem**</span><span class="sxs-lookup"><span data-stu-id="bab00-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="bab00-127">Gibt das angegebene Medien Element wieder.</span><span class="sxs-lookup"><span data-stu-id="bab00-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="bab00-128">**vorher**</span><span class="sxs-lookup"><span data-stu-id="bab00-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="bab00-129">Legt das vorherige Element in der Wiedergabeliste als Aktuelles Element fest.</span><span class="sxs-lookup"><span data-stu-id="bab00-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="bab00-130">**anzuhalten**</span><span class="sxs-lookup"><span data-stu-id="bab00-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="bab00-131">Beendet die Wiedergabe des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="bab00-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="bab00-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bab00-132">Properties</span></span>

<span data-ttu-id="bab00-133">Die **iwmpcontrols-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bab00-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="bab00-134">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bab00-134">Property</span></span>                                                                                                    | <span data-ttu-id="bab00-135">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="bab00-135">Access type</span></span>           | <span data-ttu-id="bab00-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bab00-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bab00-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="bab00-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="bab00-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bab00-138">Read/write</span></span><br/> | <span data-ttu-id="bab00-139">Ruft das aktuelle Medien Element in einer Wiedergabeliste ab oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="bab00-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="bab00-140">**currentmarker**</span><span class="sxs-lookup"><span data-stu-id="bab00-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="bab00-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bab00-141">Read/write</span></span><br/> | <span data-ttu-id="bab00-142">Ruft die aktuelle Markernummer ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="bab00-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="bab00-143">**CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="bab00-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="bab00-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bab00-144">Read/write</span></span><br/> | <span data-ttu-id="bab00-145">Ruft die aktuelle Position im Medien Element in Sekunden ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="bab00-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="bab00-146">**currentpositionstring**</span><span class="sxs-lookup"><span data-stu-id="bab00-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="bab00-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bab00-147">Read-only</span></span><br/>  | <span data-ttu-id="bab00-148">Ruft die aktuelle Position im Medien Element als **System. String** ab.</span><span class="sxs-lookup"><span data-stu-id="bab00-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="bab00-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="bab00-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="bab00-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bab00-150">Read-only</span></span><br/>  | <span data-ttu-id="bab00-151">Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bab00-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="bab00-152">In c# ist dies die **get \_ IsAvailable** -Methode.</span><span class="sxs-lookup"><span data-stu-id="bab00-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="bab00-153">Verwenden Sie die folgende Eigenschaft, um eine **iwmpcontrols** -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bab00-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="bab00-154">Object</span><span class="sxs-lookup"><span data-stu-id="bab00-154">Object</span></span>                                                                   | <span data-ttu-id="bab00-155">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bab00-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="bab00-156">AxWindowsMediaPlayer-Objekt</span><span class="sxs-lookup"><span data-stu-id="bab00-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="bab00-157">**CTL-Steuerelemente**</span><span class="sxs-lookup"><span data-stu-id="bab00-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="bab00-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bab00-158">Requirements</span></span>



| <span data-ttu-id="bab00-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bab00-159">Requirement</span></span> | <span data-ttu-id="bab00-160">Wert</span><span class="sxs-lookup"><span data-stu-id="bab00-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bab00-161">Header</span><span class="sxs-lookup"><span data-stu-id="bab00-161">Header</span></span><br/> | <dl> <span data-ttu-id="bab00-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab00-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab00-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bab00-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab00-164">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="bab00-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="bab00-165">**IWMPControls2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="bab00-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bab00-166">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="bab00-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





