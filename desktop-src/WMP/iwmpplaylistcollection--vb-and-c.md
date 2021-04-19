---
title: Iwmpplaylistcollection-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden zum Bearbeiten von iwmpwiedergabe-und iwmpplaylistarray-Schnittstellen in einer-Auflistung bereit.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Iwmpplaylistcollection (VB und C) Interface Windows Media Player
- Iwmpplaylistcollection (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369397"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="3153b-105">Iwmpplaylistcollection-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="3153b-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="3153b-106">Stellt Methoden zum Bearbeiten von **iwmpwiedergabe** -und **iwmpplaylistarray** -Schnittstellen in einer-Auflistung bereit.</span><span class="sxs-lookup"><span data-stu-id="3153b-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="3153b-107">Member</span><span class="sxs-lookup"><span data-stu-id="3153b-107">Members</span></span>

<span data-ttu-id="3153b-108">Die **iwmpplaylistcollection-Schnittstelle (VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3153b-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="3153b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="3153b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3153b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="3153b-110">Methods</span></span>

<span data-ttu-id="3153b-111">Die **iwmpplaylistcollection-Schnittstelle (VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3153b-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="3153b-112">Methode</span><span class="sxs-lookup"><span data-stu-id="3153b-112">Method</span></span>                                                                                                 | <span data-ttu-id="3153b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3153b-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3153b-114">**"GetAll"**</span><span class="sxs-lookup"><span data-stu-id="3153b-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="3153b-115">Gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.</span><span class="sxs-lookup"><span data-stu-id="3153b-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="3153b-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="3153b-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="3153b-117">Gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf Wiedergabelisten mit dem angegebenen Namen bietet, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3153b-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="3153b-118">**importwiedergabe Liste**</span><span class="sxs-lookup"><span data-stu-id="3153b-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="3153b-119">Fügt der Bibliothek eine statische Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="3153b-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="3153b-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="3153b-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="3153b-121">Gibt einen Wert zurück, der angibt, ob sich die angegebene Wiedergabeliste im Ordner Gelöschte Elemente befindet.</span><span class="sxs-lookup"><span data-stu-id="3153b-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="3153b-122">**neue**</span><span class="sxs-lookup"><span data-stu-id="3153b-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="3153b-123">Gibt eine **iwmpwiedergabe** -Schnittstelle für eine neue, leere Wiedergabeliste in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="3153b-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="3153b-124">**aufgeh**</span><span class="sxs-lookup"><span data-stu-id="3153b-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="3153b-125">Entfernt eine Wiedergabeliste aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="3153b-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="3153b-126">**SetDeleted**</span><span class="sxs-lookup"><span data-stu-id="3153b-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="3153b-127">Wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3153b-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="3153b-128">Verwenden Sie die folgende Eigenschaft, um eine **iwmpplaylistcollection** -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3153b-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="3153b-129">Object</span><span class="sxs-lookup"><span data-stu-id="3153b-129">Object</span></span>                                                                   | <span data-ttu-id="3153b-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3153b-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3153b-131">AxWindowsMediaPlayer-Objekt</span><span class="sxs-lookup"><span data-stu-id="3153b-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="3153b-132">**playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="3153b-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="3153b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3153b-133">Requirements</span></span>



| <span data-ttu-id="3153b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3153b-134">Requirement</span></span> | <span data-ttu-id="3153b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3153b-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3153b-136">Header</span><span class="sxs-lookup"><span data-stu-id="3153b-136">Header</span></span><br/> | <dl> <span data-ttu-id="3153b-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="3153b-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3153b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3153b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3153b-139">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="3153b-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="3153b-140">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3153b-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3153b-141">**Iwmpplaylistarray-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3153b-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





