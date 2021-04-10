---
description: Tritt auf, nachdem iinkanalyzer ein icontextnode-Objekt erstellt hat.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents:: contextnoentcreated-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961241"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="2044a-103">\_Ianalysisproxyevents:: contextnoentcreated-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2044a-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="2044a-104">Tritt auf, nachdem [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextnode**](icontextnode.md) -Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2044a-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2044a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2044a-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="2044a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2044a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2044a-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2044a-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2044a-108">Der [**iinkanalyzer**](iinkanalyzer.md) , der das [**icontextnode**](icontextnode.md) -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="2044a-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-109">*pcontextnode erstellt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2044a-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2044a-110">Das neue [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2044a-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2044a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2044a-111">Return value</span></span>

<span data-ttu-id="2044a-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2044a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2044a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2044a-113">Remarks</span></span>

<span data-ttu-id="2044a-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2044a-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="2044a-115">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="2044a-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="2044a-116">Wenn [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md)erstellt, enthält der neue **icontextnode** keine Striche, enthält keine Links zu anderen **icontextnode** -Objekten, und möglicherweise sind nicht alle zugehörigen Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2044a-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="2044a-117">Außerdem wird der neue **icontextnode** am Ende der Auflistung der untergeordneten Knoten des übergeordneten Knotens hinzugefügt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="2044a-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="2044a-118">Nach diesem Ereignis kann der **iinkanalyzer** die folgenden Ereignisse aufwecken.</span><span class="sxs-lookup"><span data-stu-id="2044a-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="2044a-119">Das [**\_ ianalysisproxyevents:: strokereprodent**](-ianalysisproxyevents-strokereparented.md) -Ereignis, wenn ein Strich von einem Kontext Knoten zu einem anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="2044a-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="2044a-120">Das [**\_ ianalysisproxyevents:: contextnodelta inkadditions**](-ianalysisproxyevents-contextnodelinkadding.md) -Ereignis, wenn einem [**icontextnode**](icontextnode.md)ein [**icontextlink**](icontextlink.md) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2044a-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="2044a-121">Das [**\_ ianalysisproxyevents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) -Ereignis, wenn die Reihenfolge eines [**icontextnode**](icontextnode.md) in der Auflistung von untergeordneten Knoten des übergeordneten Knotens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2044a-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="2044a-122">Der [**iinkanalyzer**](iinkanalyzer.md) löst das [**\_ ianalysisproxyevents:: contextnodebug**](-ianalysisproxyevents-contextnodepropertiesupdated.md) -Ereignis aus, nachdem der Zustand von [**icontextnode**](icontextnode.md) für diese Analysephase aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="2044a-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="2044a-123">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2044a-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2044a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2044a-124">Requirements</span></span>



| <span data-ttu-id="2044a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2044a-125">Requirement</span></span> | <span data-ttu-id="2044a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2044a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2044a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2044a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2044a-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2044a-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2044a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2044a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2044a-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2044a-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2044a-131">Header</span><span class="sxs-lookup"><span data-stu-id="2044a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2044a-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2044a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2044a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2044a-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2044a-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2044a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2044a-136">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="2044a-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="2044a-137">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="2044a-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2044a-138">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="2044a-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2044a-139">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="2044a-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2044a-140">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="2044a-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2044a-141">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="2044a-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




