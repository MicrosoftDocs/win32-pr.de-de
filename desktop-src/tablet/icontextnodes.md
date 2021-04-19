---
description: Enthält eine Auflistung von-Objekten, die die icontextnode-Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Icontextnodes-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357351"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="9a5fa-103">Icontextnodes-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a5fa-103">IContextNodes interface</span></span>

<span data-ttu-id="9a5fa-104">Enthält eine Auflistung von-Objekten, die die [**icontextnode**](icontextnode.md) -Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="9a5fa-105">Member</span><span class="sxs-lookup"><span data-stu-id="9a5fa-105">Members</span></span>

<span data-ttu-id="9a5fa-106">Die **icontextnodes** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9a5fa-107">**Icontextnodes** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9a5fa-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="9a5fa-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a5fa-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9a5fa-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="9a5fa-109">Methods</span></span>

<span data-ttu-id="9a5fa-110">Die **icontextnodes** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="9a5fa-111">Methode</span><span class="sxs-lookup"><span data-stu-id="9a5fa-111">Method</span></span>                                                       | <span data-ttu-id="9a5fa-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a5fa-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a5fa-113">**Addcontextnode**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="9a5fa-114">Fügt dieser Auflistung ein [**icontextnode**](icontextnode.md) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="9a5fa-115">**Getcontextnode**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="9a5fa-116">Ruft das [**icontextnode**](icontextnode.md) -Objekt am angegebenen Index in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="9a5fa-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="9a5fa-118">Ruft die Anzahl der [**icontextnode**](icontextnode.md) -Objekte ab, die in dieser Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="9a5fa-119">**Removecontextnode**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="9a5fa-120">Entfernt ein [**icontextnode**](icontextnode.md) -Objekt aus dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="9a5fa-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a5fa-121">Requirements</span></span>



| <span data-ttu-id="9a5fa-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a5fa-122">Requirement</span></span> | <span data-ttu-id="9a5fa-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9a5fa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5fa-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a5fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5fa-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a5fa-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a5fa-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a5fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5fa-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a5fa-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9a5fa-128">Header</span><span class="sxs-lookup"><span data-stu-id="9a5fa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a5fa-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9a5fa-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9a5fa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9a5fa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a5fa-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a5fa-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9a5fa-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a5fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5fa-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9a5fa-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="9a5fa-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

