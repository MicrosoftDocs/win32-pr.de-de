---
description: Tritt auf, bevor das iinkanalyzer-Objekt ein icontextnode-Objekt löscht.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents:: contextnodebug-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354290"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="9945d-103">\_Ianalysisproxyevents:: contextnodebug-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9945d-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="9945d-104">Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt löscht.</span><span class="sxs-lookup"><span data-stu-id="9945d-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9945d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9945d-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="9945d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9945d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9945d-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9945d-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9945d-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt löscht.</span><span class="sxs-lookup"><span data-stu-id="9945d-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9945d-109">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9945d-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9945d-110">Das [**icontextnode**](icontextnode.md) -Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9945d-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9945d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9945d-111">Return value</span></span>

<span data-ttu-id="9945d-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9945d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9945d-113">Remarks</span></span>

<span data-ttu-id="9945d-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9945d-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="9945d-115">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md)löscht.</span><span class="sxs-lookup"><span data-stu-id="9945d-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="9945d-116">Bevor [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md)löscht, entfernt **iinkanalyzer** alle Striche aus dem Kontext Knoten und entfernt alle Verknüpfungen zu anderen Kontext Knoten.</span><span class="sxs-lookup"><span data-stu-id="9945d-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="9945d-117">Vor dem Entfernen des Kontext Knotens kann **iinkanalyzer** die folgenden Ereignisse hervorrufen.</span><span class="sxs-lookup"><span data-stu-id="9945d-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="9945d-118">Das [**\_ ianalysisproxyevents:: strokereprodent**](-ianalysisproxyevents-strokereparented.md) -Ereignis, wenn es einen Strich aus dem [**icontextnode**](icontextnode.md)verschiebt.</span><span class="sxs-lookup"><span data-stu-id="9945d-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="9945d-119">Das [**\_ ianalysisproxyevents:: contextnodelinklösch**](-ianalysisproxyevents-contextnodelinkdeleting.md) -Ereignis, bevor ein [**icontextlink**](icontextlink.md) aus dem [**icontextnode**](icontextnode.md)entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9945d-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="9945d-120">Das **\_ ianalysisproxyevents:: contextnodelösch** -Ereignis, bevor ein übergeordneter Kontext Knoten entfernt wird, der keine untergeordneten Knoten mehr aufweist.</span><span class="sxs-lookup"><span data-stu-id="9945d-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="9945d-121">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9945d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9945d-122">Requirements</span></span>



| <span data-ttu-id="9945d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9945d-123">Requirement</span></span> | <span data-ttu-id="9945d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9945d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9945d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9945d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9945d-126">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9945d-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9945d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9945d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9945d-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9945d-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9945d-129">Header</span><span class="sxs-lookup"><span data-stu-id="9945d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9945d-130"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9945d-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9945d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9945d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9945d-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9945d-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9945d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9945d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9945d-134">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="9945d-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="9945d-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="9945d-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9945d-136">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="9945d-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9945d-137">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="9945d-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="9945d-138">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="9945d-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="9945d-139">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="9945d-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




