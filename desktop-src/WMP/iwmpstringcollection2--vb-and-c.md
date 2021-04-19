---
title: IWMPStringCollection2-Schnittstelle (VB und C) (WMP. h)
description: Stellt Methoden bereit, die die iwmpstringcollection-Schnittstelle ergänzen.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB und C) Interface Windows Media Player
- IWMPStringCollection2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367078"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="a04ca-105">IWMPStringCollection2-Schnittstelle (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="a04ca-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="a04ca-106">Stellt Methoden bereit, die die **iwmpstringcollection** -Schnittstelle ergänzen.</span><span class="sxs-lookup"><span data-stu-id="a04ca-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="a04ca-107">Member</span><span class="sxs-lookup"><span data-stu-id="a04ca-107">Members</span></span>

<span data-ttu-id="a04ca-108">Die IWMPStringCollection2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a04ca-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="a04ca-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="a04ca-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a04ca-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="a04ca-110">Methods</span></span>

<span data-ttu-id="a04ca-111">Die IWMPStringCollection2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="a04ca-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="a04ca-112">Methode</span><span class="sxs-lookup"><span data-stu-id="a04ca-112">Method</span></span>                                                                                                                 | <span data-ttu-id="a04ca-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a04ca-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a04ca-114">**getattributecountrytbytype**</span><span class="sxs-lookup"><span data-stu-id="a04ca-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="a04ca-115">Gibt die Anzahl der Attribute zurück, die dem angegebenen Index des Zeichen folgen Auflistungs Elements, dem Attributnamen und der Sprache zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a04ca-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="a04ca-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a04ca-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="a04ca-117">Gibt die Zeichenfolge zurück, die dem angegebenen Index und Namen des Zeichen folgen-Sammlungs Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="a04ca-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="a04ca-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="a04ca-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="a04ca-119">Gibt den Wert zurück, der dem angegebenen Index, Namen, der Sprache und dem Attribut Index für Zeichen folgen Auflistungs Elemente entspricht.</span><span class="sxs-lookup"><span data-stu-id="a04ca-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="a04ca-120">**isidentical**</span><span class="sxs-lookup"><span data-stu-id="a04ca-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="a04ca-121">Gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a04ca-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="a04ca-122">Sie erhalten eine **IWMPStringCollection2** -Schnittstelle durch Umwandeln des Werts, der von der [**iwmpmediacollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a04ca-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04ca-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a04ca-123">Requirements</span></span>



| <span data-ttu-id="a04ca-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a04ca-124">Requirement</span></span> | <span data-ttu-id="a04ca-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a04ca-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a04ca-126">Header</span><span class="sxs-lookup"><span data-stu-id="a04ca-126">Header</span></span><br/> | <dl> <span data-ttu-id="a04ca-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04ca-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04ca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a04ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04ca-129">**Schnittstellen für Visual Basic .net und C #**</span><span class="sxs-lookup"><span data-stu-id="a04ca-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="a04ca-130">**Iwmpstringcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a04ca-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





