---
description: Tritt auf, bevor das iinkanalyzer-Objekt durch Ändern des übergeordneten Knotens verschoben wird.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: '_IAnalysisProxyEvents:: contextnoderethenting-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363047"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="d3051-103">\_Ianalysisproxyevents:: contextnoderesienting-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d3051-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="d3051-104">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) [**-Objekt durch**](icontextnode.md) Ändern des übergeordneten Knotens verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d3051-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3051-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3051-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="d3051-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3051-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3051-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3051-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt verschiebt.</span><span class="sxs-lookup"><span data-stu-id="d3051-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3051-109">*pnewparameentcontextnode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3051-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3051-110">Das neue übergeordnete [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3051-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3051-111">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3051-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3051-112">Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3051-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3051-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3051-113">Return value</span></span>

<span data-ttu-id="d3051-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d3051-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3051-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3051-115">Remarks</span></span>

<span data-ttu-id="d3051-116">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3051-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d3051-117">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Methode auf, die einen [**icontextnode**](icontextnode.md) aus einer Auflistung von untergeordneten Knoten zu einem anderen verschiebt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="d3051-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="d3051-118">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d3051-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3051-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3051-119">Requirements</span></span>



| <span data-ttu-id="d3051-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3051-120">Requirement</span></span> | <span data-ttu-id="d3051-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3051-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3051-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3051-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3051-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3051-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d3051-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3051-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3051-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d3051-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d3051-126">Header</span><span class="sxs-lookup"><span data-stu-id="d3051-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3051-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d3051-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d3051-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d3051-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3051-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3051-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d3051-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3051-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3051-131">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="d3051-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d3051-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="d3051-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d3051-133">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="d3051-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d3051-134">**Icontextnode:: getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="d3051-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="d3051-135">**Icontextnode:: getsubnodes**</span><span class="sxs-lookup"><span data-stu-id="d3051-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="d3051-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="d3051-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d3051-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="d3051-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d3051-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d3051-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




