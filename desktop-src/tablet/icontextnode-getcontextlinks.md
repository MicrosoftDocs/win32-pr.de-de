---
description: Ruft eine Auflistung von icontextlink-Objekten ab, die Beziehungen mit anderen icontextnode-Objekten darstellt.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Icontextnode:: getcontextlinks-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372837"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="837ec-103">Icontextnode:: getcontextlinks-Methode</span><span class="sxs-lookup"><span data-stu-id="837ec-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="837ec-104">Ruft eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten ab, die Beziehungen mit anderen [**icontextnode**](icontextnode.md) -Objekten darstellt.</span><span class="sxs-lookup"><span data-stu-id="837ec-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="837ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="837ec-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="837ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="837ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="837ec-107">*ppcontextlinks* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="837ec-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="837ec-108">Ein Zeiger auf eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten, die Beziehungen zu anderen [**icontextnode**](icontextnode.md) -Objekten darstellt.</span><span class="sxs-lookup"><span data-stu-id="837ec-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="837ec-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="837ec-109">Return value</span></span>

<span data-ttu-id="837ec-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="837ec-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="837ec-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="837ec-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="837ec-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppcontextlinks* , wenn Sie die Auflistung der Kontext Verknüpfungen nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="837ec-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="837ec-113">Um Informationen über Beziehungen zwischen übergeordneten und untergeordneten Knoten zu erhalten, verwenden Sie [**icontextnode:: getParser Node**](icontextnode-getparentnode.md) oder [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="837ec-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="837ec-114">Weitere Informationen zu den Arten von Beziehungen, die durch Links beschrieben werden, finden Sie unter [**icontextlink**](icontextlink.md) und [**ContextLinkDirection**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="837ec-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="837ec-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="837ec-115">Requirements</span></span>



| <span data-ttu-id="837ec-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="837ec-116">Requirement</span></span> | <span data-ttu-id="837ec-117">Wert</span><span class="sxs-lookup"><span data-stu-id="837ec-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837ec-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="837ec-118">Minimum supported client</span></span><br/> | <span data-ttu-id="837ec-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="837ec-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="837ec-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="837ec-120">Minimum supported server</span></span><br/> | <span data-ttu-id="837ec-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="837ec-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="837ec-122">Header</span><span class="sxs-lookup"><span data-stu-id="837ec-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="837ec-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="837ec-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="837ec-124">DLL</span><span class="sxs-lookup"><span data-stu-id="837ec-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="837ec-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837ec-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="837ec-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="837ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837ec-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="837ec-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="837ec-128">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="837ec-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="837ec-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="837ec-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="837ec-130">**Icontextnode:: addcontextlink**</span><span class="sxs-lookup"><span data-stu-id="837ec-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="837ec-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="837ec-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

