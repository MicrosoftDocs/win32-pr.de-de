---
title: IWMPPlaylist (VB und C )-Schnittstelle (Wmp.h)
description: Stellt Eigenschaften und Methoden bereit, um Medienelemente in einer Wiedergabeliste zu organisieren, zu verwalten und zu bearbeiten. Die iwmpwiedergabe-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Media Player der iwmpwiedergabe-Schnittstelle (VB und C)
- Windows Media Player der iwmpwiedergabe-Schnittstelle (VB und C), beschrieben
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365669"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a><span data-ttu-id="01040-105">Iwmpwiedergabe-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="01040-105">IWMPPlaylist (VB and C#) interface</span></span>

<span data-ttu-id="01040-106">Stellt Eigenschaften und Methoden bereit, um Medienelemente in einer Wiedergabeliste zu organisieren, zu verwalten und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="01040-106">Provides properties and methods to organize, manage, and manipulate media items in a playlist.</span></span>

<span data-ttu-id="01040-107">Die **iwmpwiedergabe** -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="01040-107">The **IWMPPlaylist** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="01040-108">Member</span><span class="sxs-lookup"><span data-stu-id="01040-108">Members</span></span>

<span data-ttu-id="01040-109">Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="01040-109">The **IWMPPlaylist (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="01040-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="01040-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="01040-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01040-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01040-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="01040-112">Methods</span></span>

<span data-ttu-id="01040-113">Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="01040-113">The **IWMPPlaylist (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="01040-114">Methode</span><span class="sxs-lookup"><span data-stu-id="01040-114">Method</span></span>                                                                       | <span data-ttu-id="01040-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01040-115">Description</span></span>                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="01040-116">**appendItem**</span><span class="sxs-lookup"><span data-stu-id="01040-116">**appendItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | <span data-ttu-id="01040-117">Fügt ein Medien Element am Ende der Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="01040-117">Adds a media item to the end of the playlist.</span></span><br/>                |
| [<span data-ttu-id="01040-118">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="01040-118">**clear**</span></span>](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | <span data-ttu-id="01040-119">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="01040-119">Reserved for future use.</span></span><br/>                                     |
| [<span data-ttu-id="01040-120">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="01040-120">**getItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | <span data-ttu-id="01040-121">Gibt den Wert eines durch den Namen angegebenen Wiedergabelisten Attributs zurück.</span><span class="sxs-lookup"><span data-stu-id="01040-121">Returns the value of a playlist attribute specified by name.</span></span><br/> |
| [<span data-ttu-id="01040-122">**insertItem**</span><span class="sxs-lookup"><span data-stu-id="01040-122">**insertItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | <span data-ttu-id="01040-123">Fügt ein Medien Element an einem angegebenen Speicherort in eine Wiedergabeliste ein.</span><span class="sxs-lookup"><span data-stu-id="01040-123">Inserts a media item at a specified location in a playlist.</span></span><br/>  |
| [<span data-ttu-id="01040-124">**"muveitem"**</span><span class="sxs-lookup"><span data-stu-id="01040-124">**moveItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | <span data-ttu-id="01040-125">Ändert den Speicherort eines Medien Elements in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="01040-125">Changes the location of a media item in the playlist.</span></span><br/>        |
| [<span data-ttu-id="01040-126">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="01040-126">**removeItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | <span data-ttu-id="01040-127">Entfernt das angegebene Medien Element aus der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="01040-127">Removes the specified media item from the playlist.</span></span><br/>          |
| [<span data-ttu-id="01040-128">**"Einstellungs Element"**</span><span class="sxs-lookup"><span data-stu-id="01040-128">**setItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | <span data-ttu-id="01040-129">Legt den Wert eines Wiedergabelisten Attributs fest.</span><span class="sxs-lookup"><span data-stu-id="01040-129">Sets the value of a playlist attribute.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="01040-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="01040-130">Properties</span></span>

<span data-ttu-id="01040-131">Die **iwmpwiedergabe-Schnittstelle (VB und c#)** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="01040-131">The **IWMPPlaylist (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="01040-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01040-132">Property</span></span>                                                                                      | <span data-ttu-id="01040-133">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="01040-133">Access type</span></span>           | <span data-ttu-id="01040-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01040-134">Description</span></span>                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01040-135">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="01040-135">**attributeCount**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | <span data-ttu-id="01040-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01040-136">Read-only</span></span><br/>  | <span data-ttu-id="01040-137">Ruft die Anzahl der einer Wiedergabeliste zugeordneten Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="01040-137">Gets the number of attributes associated with a playlist.</span></span><br/>                                                                                |
| [<span data-ttu-id="01040-138">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="01040-138">**attributeName**</span></span>](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | <span data-ttu-id="01040-139">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01040-139">Read-only</span></span><br/>  | <span data-ttu-id="01040-140">Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="01040-140">Gets the name of a playlist attribute specified by an index.</span></span> <span data-ttu-id="01040-141">In c# ist dies die get \_ attributeName-Methode.</span><span class="sxs-lookup"><span data-stu-id="01040-141">In C# this is the get\_attributeName method.</span></span><br/>                               |
| [<span data-ttu-id="01040-142">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="01040-142">**count**</span></span>](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | <span data-ttu-id="01040-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01040-143">Read-only</span></span><br/>  | <span data-ttu-id="01040-144">Ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.</span><span class="sxs-lookup"><span data-stu-id="01040-144">Gets the number of media items in a playlist.</span></span><br/>                                                                                            |
| [<span data-ttu-id="01040-145">**isidentical**</span><span class="sxs-lookup"><span data-stu-id="01040-145">**isIdentical**</span></span>](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | <span data-ttu-id="01040-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01040-146">Read-only</span></span><br/>  | <span data-ttu-id="01040-147">Ruft einen Wert ab, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist.</span><span class="sxs-lookup"><span data-stu-id="01040-147">Gets a value indicating whether the specified playlist is identical to the current playlist.</span></span> <span data-ttu-id="01040-148">In c# ist dies die get \_ isidentical-Methode.</span><span class="sxs-lookup"><span data-stu-id="01040-148">In C# this is the get\_isIdentical method.</span></span><br/> |
| [<span data-ttu-id="01040-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="01040-149">**Item**</span></span>](iwmpplaylist-item--vb-and-c.md)<br/>                                        | <span data-ttu-id="01040-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="01040-150">Read-only</span></span><br/>  | <span data-ttu-id="01040-151">Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="01040-151">Gets an interface to the media item at the specified index.</span></span> <span data-ttu-id="01040-152">In c# ist dies die get \_ Item-Methode.</span><span class="sxs-lookup"><span data-stu-id="01040-152">In C# this is the get\_Item method.</span></span><br/>                                         |
| [<span data-ttu-id="01040-153">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="01040-153">**name**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | <span data-ttu-id="01040-154">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="01040-154">Read/write</span></span><br/> | <span data-ttu-id="01040-155">Ruft den Namen der Wiedergabeliste ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="01040-155">Gets or sets the name of the playlist.</span></span><br/>                                                                                                   |



 

<span data-ttu-id="01040-156">Abrufen einer **iwmpwiedergabe** -Schnittstelle mithilfe der folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="01040-156">Get an **IWMPPlaylist** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="01040-157">Objekt oder Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="01040-157">Object or interface</span></span>                                                | <span data-ttu-id="01040-158">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="01040-158">Property or method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01040-159">**Iwmpcdrom**</span><span class="sxs-lookup"><span data-stu-id="01040-159">**IWMPCdrom**</span></span>](iwmpcdrom--vb-and-c.md)                           | [<span data-ttu-id="01040-160">**Abspielen**</span><span class="sxs-lookup"><span data-stu-id="01040-160">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="01040-161">**Iwmpmediacollection**</span><span class="sxs-lookup"><span data-stu-id="01040-161">**IWMPMediaCollection**</span></span>](iwmpmediacollection--vb-and-c.md)       | <span data-ttu-id="01040-162">[**GetAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getbyalbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getbyattribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getbyauthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getbygenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="01040-162">[**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span></span> |
| [<span data-ttu-id="01040-163">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="01040-163">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md)  | <span data-ttu-id="01040-164">[**currentwiedergabe**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newwiedergabe**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="01040-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [**newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="01040-165">**Iwmpplaylistarray**</span><span class="sxs-lookup"><span data-stu-id="01040-165">**IWMPPlaylistArray**</span></span>](iwmpplaylistarray--vb-and-c.md)           | [<span data-ttu-id="01040-166">**Element**</span><span class="sxs-lookup"><span data-stu-id="01040-166">**Item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="01040-167">**Iwmpplaylistcollection**</span><span class="sxs-lookup"><span data-stu-id="01040-167">**IWMPPlaylistCollection**</span></span>](iwmpplaylistcollection--vb-and-c.md) | [<span data-ttu-id="01040-168">**neue**</span><span class="sxs-lookup"><span data-stu-id="01040-168">**newPlaylist**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="01040-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01040-169">Requirements</span></span>



| <span data-ttu-id="01040-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01040-170">Requirement</span></span> | <span data-ttu-id="01040-171">Wert</span><span class="sxs-lookup"><span data-stu-id="01040-171">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01040-172">Header</span><span class="sxs-lookup"><span data-stu-id="01040-172">Header</span></span><br/> | <dl> <span data-ttu-id="01040-173"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="01040-173"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01040-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01040-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01040-175">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="01040-175">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





