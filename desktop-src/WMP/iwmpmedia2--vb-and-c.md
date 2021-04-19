---
title: IWMPMedia2-Schnittstelle (VB und C) (WMP. h)
description: Ermöglicht den Zugriff auf eine zusätzliche Medien Element Eigenschaft.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB und C) Interface Windows Media Player
- IWMPMedia2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364428"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="033ab-105">IWMPMedia2-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="033ab-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="033ab-106">Ermöglicht den Zugriff auf eine zusätzliche Medien Element Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="033ab-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="033ab-107">Zusätzlich zu den Eigenschaften und Methoden, die von **iwmpmedia** geerbt werden, macht die **IWMPMedia2** -Schnittstelle die folgende Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="033ab-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="033ab-108">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="033ab-108">Property</span></span>                                                 | <span data-ttu-id="033ab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="033ab-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="033ab-110">Fehler</span><span class="sxs-lookup"><span data-stu-id="033ab-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="033ab-111">Ruft eine **iwmperroritem** -Schnittstelle ab, wenn das Medien Element einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="033ab-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="033ab-112">Abrufen einer **IWMPMedia2** -Schnittstelle durch Umwandeln des Werts, der von einer der folgenden Eigenschaften oder Methoden zurückgegeben wird, auf die über das folgende Objekt oder die folgende Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="033ab-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="033ab-113">Objekt oder Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="033ab-113">Object or interface</span></span>                                               | <span data-ttu-id="033ab-114">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="033ab-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="033ab-115">Iwmpcontrols</span><span class="sxs-lookup"><span data-stu-id="033ab-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="033ab-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="033ab-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="033ab-117">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="033ab-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="033ab-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newmedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="033ab-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="033ab-119">Iwmpwiedergabe</span><span class="sxs-lookup"><span data-stu-id="033ab-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="033ab-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **\_ Element** in c# Get)</span><span class="sxs-lookup"><span data-stu-id="033ab-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="033ab-121">Member</span><span class="sxs-lookup"><span data-stu-id="033ab-121">Members</span></span>

<span data-ttu-id="033ab-122">Die **IWMPMedia2-Schnittstelle (VB und c#)** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="033ab-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="033ab-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="033ab-123">Requirements</span></span>



| <span data-ttu-id="033ab-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="033ab-124">Requirement</span></span> | <span data-ttu-id="033ab-125">Wert</span><span class="sxs-lookup"><span data-stu-id="033ab-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="033ab-126">Header</span><span class="sxs-lookup"><span data-stu-id="033ab-126">Header</span></span><br/> | <dl> <span data-ttu-id="033ab-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="033ab-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="033ab-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="033ab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033ab-129">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="033ab-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="033ab-130">**Iwmperroritem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="033ab-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="033ab-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="033ab-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="033ab-132">**IWMPMedia3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="033ab-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





