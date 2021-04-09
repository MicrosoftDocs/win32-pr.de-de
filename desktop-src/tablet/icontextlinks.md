---
description: Enthält eine Auflistung von-Objekten, die die icontextlink-Schnittstelle implementieren.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Icontextlinks-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958976"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="f212a-103">Icontextlinks-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f212a-103">IContextLinks interface</span></span>

<span data-ttu-id="f212a-104">Enthält eine Auflistung von-Objekten, die die [**icontextlink**](icontextlink.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f212a-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="f212a-105">Member</span><span class="sxs-lookup"><span data-stu-id="f212a-105">Members</span></span>

<span data-ttu-id="f212a-106">Die **icontextlinks** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f212a-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f212a-107">**Icontextlinks** enthält auch die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f212a-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="f212a-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f212a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f212a-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f212a-109">Methods</span></span>

<span data-ttu-id="f212a-110">Die **icontextlinks** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f212a-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="f212a-111">Methode</span><span class="sxs-lookup"><span data-stu-id="f212a-111">Method</span></span>                                                 | <span data-ttu-id="f212a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f212a-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f212a-113">**Getcontextlink**</span><span class="sxs-lookup"><span data-stu-id="f212a-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="f212a-114">Ruft den [**icontextlink**](icontextlink.md) am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="f212a-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="f212a-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="f212a-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="f212a-116">Ruft die Anzahl der [**icontextlink**](icontextlink.md) -Objekte in dieser Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="f212a-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f212a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f212a-117">Remarks</span></span>

<span data-ttu-id="f212a-118">Der Zugriff erfolgt in der Regel über die [**icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f212a-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f212a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f212a-119">Requirements</span></span>



| <span data-ttu-id="f212a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f212a-120">Requirement</span></span> | <span data-ttu-id="f212a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f212a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f212a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f212a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f212a-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f212a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f212a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f212a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f212a-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f212a-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f212a-126">Header</span><span class="sxs-lookup"><span data-stu-id="f212a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f212a-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f212a-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f212a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f212a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f212a-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f212a-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f212a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f212a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f212a-131">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="f212a-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="f212a-132">**Icontextnode:: addcontextlink**</span><span class="sxs-lookup"><span data-stu-id="f212a-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="f212a-133">**Icontextnode::D eletecontextlink**</span><span class="sxs-lookup"><span data-stu-id="f212a-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="f212a-134">**Icontextnode:: getcontextlinks**</span><span class="sxs-lookup"><span data-stu-id="f212a-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="f212a-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f212a-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

