---
title: IWMPMedia3-Schnittstelle (VB und C) (WMP. h)
description: Stellt zusätzliche Methoden für den Zugriff auf die Eigenschaften eines Medien Elements bereit.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- IWMPMedia3 (VB und C) Interface Windows Media Player
- IWMPMedia3 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373593"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a><span data-ttu-id="758e3-105">IWMPMedia3-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="758e3-105">IWMPMedia3 (VB and C#) interface</span></span>

<span data-ttu-id="758e3-106">Stellt zusätzliche Methoden für den Zugriff auf die Eigenschaften eines Medien Elements bereit.</span><span class="sxs-lookup"><span data-stu-id="758e3-106">Provides additional methods to access the properties of a media item.</span></span>

## <a name="members"></a><span data-ttu-id="758e3-107">Member</span><span class="sxs-lookup"><span data-stu-id="758e3-107">Members</span></span>

<span data-ttu-id="758e3-108">Die IWMPMedia3-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="758e3-108">The **IWMPMedia3 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="758e3-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="758e3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="758e3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="758e3-110">Methods</span></span>

<span data-ttu-id="758e3-111">Die IWMPMedia3-Schnittstelle **(VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="758e3-111">The **IWMPMedia3 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="758e3-112">Methode</span><span class="sxs-lookup"><span data-stu-id="758e3-112">Method</span></span>                                                                                           | <span data-ttu-id="758e3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="758e3-113">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="758e3-114">**getattributecountrytbytype**</span><span class="sxs-lookup"><span data-stu-id="758e3-114">**getAttributeCountByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="758e3-115">Gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="758e3-115">Returns the number of attributes associated with the specified attribute type.</span></span><br/>              |
| [<span data-ttu-id="758e3-116">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="758e3-116">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="758e3-117">Gibt den Wert des Attributs zurück, das dem angegebenen Attributtyp und Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="758e3-117">Returns the value of the attribute corresponding to the specified attribute type and index.</span></span><br/> |



 

<span data-ttu-id="758e3-118">Abrufen einer **IWMPMedia3** -Schnittstelle durch Umwandeln des Werts, der von einer der folgenden Eigenschaften oder Methoden zurückgegeben wird, auf die über das folgende Objekt oder die folgende Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="758e3-118">Get an **IWMPMedia3** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="758e3-119">Objekt oder Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="758e3-119">Object or interface</span></span>                                               | <span data-ttu-id="758e3-120">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="758e3-120">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="758e3-121">Iwmpcontrols</span><span class="sxs-lookup"><span data-stu-id="758e3-121">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="758e3-122">currentItem</span><span class="sxs-lookup"><span data-stu-id="758e3-122">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="758e3-123">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="758e3-123">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="758e3-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newmedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="758e3-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="758e3-125">Iwmpwiedergabe</span><span class="sxs-lookup"><span data-stu-id="758e3-125">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="758e3-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **\_ Element** in c# Get)</span><span class="sxs-lookup"><span data-stu-id="758e3-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="758e3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="758e3-127">Requirements</span></span>



| <span data-ttu-id="758e3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="758e3-128">Requirement</span></span> | <span data-ttu-id="758e3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="758e3-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="758e3-130">Header</span><span class="sxs-lookup"><span data-stu-id="758e3-130">Header</span></span><br/> | <dl> <span data-ttu-id="758e3-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="758e3-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="758e3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="758e3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758e3-133">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="758e3-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="758e3-134">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="758e3-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="758e3-135">**IWMPMedia2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="758e3-135">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





