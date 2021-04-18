---
description: Fügt der Auflistung von Kontext Verknüpfungen des icontextnode-Objekts einen neuen icontextlink hinzu.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'Icontextnode:: addcontextlink-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345124"
---
# <a name="icontextnodeaddcontextlink-method"></a><span data-ttu-id="7f08d-103">Icontextnode:: addcontextlink-Methode</span><span class="sxs-lookup"><span data-stu-id="7f08d-103">IContextNode::AddContextLink method</span></span>

<span data-ttu-id="7f08d-104">Fügt der Auflistung von Kontext Verknüpfungen des [**icontextnode**](icontextnode.md) -Objekts einen neuen [**icontextlink**](icontextlink.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f08d-104">Adds a new [**IContextLink**](icontextlink.md) to the [**IContextNode**](icontextnode.md) object's collection of context links.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f08d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f08d-105">Syntax</span></span>


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a><span data-ttu-id="7f08d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f08d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f08d-107">*pdestinationnode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f08d-107">*pDestinationNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-108">Der [**icontextnode**](icontextnode.md) -Zielknoten für den neuen [**icontextlink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="7f08d-108">The destination [**IContextNode**](icontextnode.md) for the new [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-109">*LinkDirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f08d-109">*linkDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-110">Die Richtung des zu erstellenden [**icontextlink**](icontextlink.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f08d-110">The direction of [**IContextLink**](icontextlink.md) object to create.</span></span>

</dd> <dt>

<span data-ttu-id="7f08d-111">*ppcontextlinkto Add* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7f08d-111">*ppContextLinkToAdd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f08d-112">Ein Zeiger auf das neue [**icontextlink**](icontextlink.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f08d-112">A pointer to the new [**IContextLink**](icontextlink.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f08d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f08d-113">Return value</span></span>

<span data-ttu-id="7f08d-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7f08d-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f08d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f08d-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7f08d-116">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextlinkdeadd* , wenn Sie den Kontext Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="7f08d-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinkToAdd* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="7f08d-117">Dieses [**icontextnode**](icontextnode.md) -Objekt ist der Quellknoten (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md)) für das neue [**icontextlink**](icontextlink.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7f08d-117">This [**IContextNode**](icontextnode.md) object is the source node (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)) for the new [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f08d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f08d-118">Requirements</span></span>



| <span data-ttu-id="7f08d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f08d-119">Requirement</span></span> | <span data-ttu-id="7f08d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7f08d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f08d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f08d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f08d-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f08d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f08d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f08d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f08d-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f08d-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7f08d-125">Header</span><span class="sxs-lookup"><span data-stu-id="7f08d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f08d-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f08d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f08d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f08d-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7f08d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f08d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f08d-130">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="7f08d-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7f08d-131">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="7f08d-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="7f08d-132">**Icontextlinks**</span><span class="sxs-lookup"><span data-stu-id="7f08d-132">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="7f08d-133">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="7f08d-133">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="7f08d-134">**Icontextnode::D eletecontextlink**</span><span class="sxs-lookup"><span data-stu-id="7f08d-134">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="7f08d-135">**Icontextnode:: getcontextlinks**</span><span class="sxs-lookup"><span data-stu-id="7f08d-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="7f08d-136">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="7f08d-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

