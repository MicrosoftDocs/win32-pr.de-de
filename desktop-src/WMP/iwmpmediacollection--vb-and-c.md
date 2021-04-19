---
title: Iwmpmediacollection-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden bereit, die verwendet werden können, um eine große Auflistung von Medien Elementen zu organisieren.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Iwmpmediacollection (VB und C) Interface Windows Media Player
- Iwmpmediacollection (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370945"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="88062-105">Iwmpmediacollection-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="88062-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="88062-106">Stellt Methoden bereit, die verwendet werden können, um eine große Auflistung von Medien Elementen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="88062-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="88062-107">Member</span><span class="sxs-lookup"><span data-stu-id="88062-107">Members</span></span>

<span data-ttu-id="88062-108">Die **iwmpmediacollection-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="88062-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="88062-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="88062-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="88062-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="88062-110">Methods</span></span>

<span data-ttu-id="88062-111">Die **iwmpmediacollection-Schnittstelle (VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="88062-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="88062-112">Methode</span><span class="sxs-lookup"><span data-stu-id="88062-112">Method</span></span>                                                                                                                       | <span data-ttu-id="88062-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88062-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88062-114">**add**</span><span class="sxs-lookup"><span data-stu-id="88062-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="88062-115">Fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="88062-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="88062-116">**"GetAll"**</span><span class="sxs-lookup"><span data-stu-id="88062-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="88062-117">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die der Wiedergabeliste entspricht, die alle Medienelemente in der Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="88062-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="88062-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="88062-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="88062-119">Gibt eine **iwmpstringcollection** -Schnittstelle zurück, die den Satz aller Werte für ein angegebenes Attribut innerhalb eines Medientyps darstellt.</span><span class="sxs-lookup"><span data-stu-id="88062-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="88062-120">**getbyalbum**</span><span class="sxs-lookup"><span data-stu-id="88062-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="88062-121">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="88062-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="88062-122">**getbyattribute**</span><span class="sxs-lookup"><span data-stu-id="88062-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="88062-123">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die dem angegebenen Attribut mit dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="88062-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="88062-124">**getbyauthor**</span><span class="sxs-lookup"><span data-stu-id="88062-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="88062-125">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="88062-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="88062-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="88062-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="88062-127">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="88062-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="88062-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="88062-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="88062-129">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit dem angegebenen Namen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="88062-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="88062-130">**getmediaatom**</span><span class="sxs-lookup"><span data-stu-id="88062-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="88062-131">Gibt den Index eines angegebenen Attributs zurück.</span><span class="sxs-lookup"><span data-stu-id="88062-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="88062-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="88062-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="88062-133">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88062-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="88062-134">**aufgeh**</span><span class="sxs-lookup"><span data-stu-id="88062-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="88062-135">Entfernt das angegebene Medien Element aus der Medien Auflistung.</span><span class="sxs-lookup"><span data-stu-id="88062-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="88062-136">**SetDeleted**</span><span class="sxs-lookup"><span data-stu-id="88062-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="88062-137">Verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="88062-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="88062-138">Sie erhalten eine **iwmpmediacollection** -Schnittstelle mit den folgenden Eigenschaften, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="88062-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="88062-139">Objekt oder Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="88062-139">Object or interface</span></span>                                               | <span data-ttu-id="88062-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="88062-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="88062-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="88062-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="88062-142">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="88062-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="88062-143">**Iwmplibrary**</span><span class="sxs-lookup"><span data-stu-id="88062-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="88062-144">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="88062-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="88062-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88062-145">Requirements</span></span>



| <span data-ttu-id="88062-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88062-146">Requirement</span></span> | <span data-ttu-id="88062-147">Wert</span><span class="sxs-lookup"><span data-stu-id="88062-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88062-148">Header</span><span class="sxs-lookup"><span data-stu-id="88062-148">Header</span></span><br/> | <dl> <span data-ttu-id="88062-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="88062-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88062-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88062-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88062-151">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="88062-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="88062-152">**IWMPMediaCollection2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="88062-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="88062-153">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="88062-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="88062-154">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="88062-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





