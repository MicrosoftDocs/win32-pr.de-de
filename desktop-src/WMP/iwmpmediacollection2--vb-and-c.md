---
title: IWMPMediaCollection2-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden bereit, die die iwmpmediacollection-Schnittstelle ergänzen.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB und C) Interface Windows Media Player
- IWMPMediaCollection2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355937"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="109c1-105">IWMPMediaCollection2-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="109c1-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="109c1-106">Stellt Methoden bereit, die die **iwmpmediacollection** -Schnittstelle ergänzen.</span><span class="sxs-lookup"><span data-stu-id="109c1-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="109c1-107">Member</span><span class="sxs-lookup"><span data-stu-id="109c1-107">Members</span></span>

<span data-ttu-id="109c1-108">Die IWMPMediaCollection2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="109c1-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="109c1-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="109c1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="109c1-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="109c1-110">Methods</span></span>

<span data-ttu-id="109c1-111">Die IWMPMediaCollection2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="109c1-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="109c1-112">Methode</span><span class="sxs-lookup"><span data-stu-id="109c1-112">Method</span></span>                                                                                                                     | <span data-ttu-id="109c1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="109c1-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="109c1-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="109c1-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="109c1-115">Gibt eine **iwmpquery** -Schnittstelle zurück, die eine neue Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="109c1-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="109c1-116">**getbyattributeandmediatype**</span><span class="sxs-lookup"><span data-stu-id="109c1-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="109c1-117">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit einem angegebenen Attribut und Medientyp ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="109c1-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="109c1-118">**getplaylistbyquery**</span><span class="sxs-lookup"><span data-stu-id="109c1-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="109c1-119">Gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die Zugriff auf Medienelemente bietet, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="109c1-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="109c1-120">**getstringcollectionbyquery**</span><span class="sxs-lookup"><span data-stu-id="109c1-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="109c1-121">Gibt eine **iwmpstringcollection** -Schnittstelle zurück, die Zugriff auf den Satz aller Zeichen folgen Werte für ein angegebenes Attribut bietet, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="109c1-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="109c1-122">Sie erhalten eine **IWMPMediaCollection2** -Schnittstelle, indem Sie den Wert umwandeln, der von der [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) -Eigenschaft zurückgegeben wird, oder den von der [**iwmplibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) -Eigenschaft zurückgegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="109c1-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="109c1-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="109c1-123">Requirements</span></span>



| <span data-ttu-id="109c1-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="109c1-124">Requirement</span></span> | <span data-ttu-id="109c1-125">Wert</span><span class="sxs-lookup"><span data-stu-id="109c1-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="109c1-126">Header</span><span class="sxs-lookup"><span data-stu-id="109c1-126">Header</span></span><br/> | <dl> <span data-ttu-id="109c1-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="109c1-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109c1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="109c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109c1-129">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="109c1-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="109c1-130">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="109c1-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





