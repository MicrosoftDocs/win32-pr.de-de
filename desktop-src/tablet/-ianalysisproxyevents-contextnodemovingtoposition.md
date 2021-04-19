---
description: Tritt auf, bevor das iinkanalyzer-Objekt ein icontextnode-Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents:: ContextNodeMovingToPosition-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353268"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="35887-103">\_Ianalysisproxyevents:: ContextNodeMovingToPosition-Ereignis</span><span class="sxs-lookup"><span data-stu-id="35887-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="35887-104">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.</span><span class="sxs-lookup"><span data-stu-id="35887-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="35887-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35887-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="35887-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35887-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35887-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35887-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt verschiebt.</span><span class="sxs-lookup"><span data-stu-id="35887-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="35887-109">*pisubnoabtomove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35887-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35887-110">Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="35887-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="35887-111">*pparameentcontextnode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35887-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35887-112">Das übergeordnete [**icontextnode**](icontextnode.md) -Objekt von *pisubnodecotomove*.</span><span class="sxs-lookup"><span data-stu-id="35887-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="35887-113">*ulnetwindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35887-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35887-114">Die neue Position von *pisubnodetomove* in der Auflistung der untergeordneten Knoten des übergeordneten Knotens.</span><span class="sxs-lookup"><span data-stu-id="35887-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35887-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35887-115">Return value</span></span>

<span data-ttu-id="35887-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="35887-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35887-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35887-117">Remarks</span></span>

<span data-ttu-id="35887-118">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="35887-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="35887-119">Dieses Ereignis tritt während der Abstimmungsphase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md) in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="35887-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="35887-120">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="35887-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35887-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35887-121">Requirements</span></span>



| <span data-ttu-id="35887-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35887-122">Requirement</span></span> | <span data-ttu-id="35887-123">Wert</span><span class="sxs-lookup"><span data-stu-id="35887-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35887-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35887-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35887-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35887-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35887-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35887-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35887-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="35887-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="35887-128">Header</span><span class="sxs-lookup"><span data-stu-id="35887-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35887-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="35887-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="35887-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35887-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35887-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35887-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="35887-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35887-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35887-133">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="35887-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="35887-134">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="35887-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="35887-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="35887-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="35887-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="35887-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="35887-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="35887-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="35887-138">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="35887-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="35887-139">**Icontextnode:: getsubnodes**</span><span class="sxs-lookup"><span data-stu-id="35887-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="35887-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="35887-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




