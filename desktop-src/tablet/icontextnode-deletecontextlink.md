---
description: Löscht ein icontextlink-Objekt aus der Link Auflistung des icontextnode-Objekts.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: Icontextnode::D eletecontextlink-Methode (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348795"
---
# <a name="icontextnodedeletecontextlink-method"></a><span data-ttu-id="cfc74-103">Icontextnode::D eletecontextlink-Methode</span><span class="sxs-lookup"><span data-stu-id="cfc74-103">IContextNode::DeleteContextLink method</span></span>

<span data-ttu-id="cfc74-104">Löscht ein [**icontextlink**](icontextlink.md) -Objekt aus der Link Auflistung des [**icontextnode**](icontextnode.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="cfc74-104">Deletes an [**IContextLink**](icontextlink.md) object from the [**IContextNode**](icontextnode.md) object's link collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfc74-105">Syntax</span></span>


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="cfc74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfc74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc74-107">*pcontextlinkto DELETE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc74-107">*pContextLinkToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc74-108">Das zu löschende [**icontextlink**](icontextlink.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="cfc74-108">The [**IContextLink**](icontextlink.md) object to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc74-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfc74-109">Return value</span></span>

<span data-ttu-id="cfc74-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cfc74-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc74-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfc74-111">Remarks</span></span>

<span data-ttu-id="cfc74-112">Ein Kontext Link weist einen Quellknoten und einen Zielknoten auf (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md) und [**icontextlink:: getdestinationnode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc74-112">A context link has a source node and a destination node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span> <span data-ttu-id="cfc74-113">Diese Methode entfernt den [**icontextlink**](icontextlink.md) aus der Auflistung von Kontext Verknüpfungen der Quell-und Zielknoten (siehe [**icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc74-113">This method removes the [**IContextLink**](icontextlink.md) from both the source and destination nodes' collection of context links (see [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc74-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfc74-114">Requirements</span></span>



| <span data-ttu-id="cfc74-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfc74-115">Requirement</span></span> | <span data-ttu-id="cfc74-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cfc74-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc74-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfc74-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc74-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfc74-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cfc74-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfc74-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc74-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cfc74-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cfc74-121">Header</span><span class="sxs-lookup"><span data-stu-id="cfc74-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc74-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cfc74-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cfc74-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc74-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc74-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc74-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cfc74-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfc74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc74-126">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="cfc74-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cfc74-127">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="cfc74-127">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="cfc74-128">**Icontextnode:: addcontextlink**</span><span class="sxs-lookup"><span data-stu-id="cfc74-128">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="cfc74-129">**Icontextnode:: getcontextlinks**</span><span class="sxs-lookup"><span data-stu-id="cfc74-129">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="cfc74-130">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="cfc74-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




