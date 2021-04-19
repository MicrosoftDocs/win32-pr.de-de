---
description: Tritt auf, bevor der Ink Analyzer ein icontextlink-Objekt zwischen zwei icontextnode-Objekten hinzufügt.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: '_IAnalysisProxyEvents:: contextnodelta inkadditions-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366380"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="bc576-103">\_Ianalysisproxyevents:: contextnodelta inkadditions-Ereignis</span><span class="sxs-lookup"><span data-stu-id="bc576-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="bc576-104">Tritt auf, bevor der Ink Analyzer ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc576-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc576-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc576-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="bc576-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc576-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc576-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc576-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Element, das den Link hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc576-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="bc576-109">*pcontextlinkumbeadded* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc576-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc576-110">Das [**icontextlink**](icontextlink.md) -Objekt, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc576-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc576-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc576-111">Return value</span></span>

<span data-ttu-id="bc576-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bc576-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc576-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc576-113">Remarks</span></span>

<span data-ttu-id="bc576-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc576-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="bc576-115">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einem [**icontextnode**](icontextnode.md)einen neuen [**icontextlink**](icontextlink.md) hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bc576-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="bc576-116">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bc576-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc576-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc576-117">Requirements</span></span>



| <span data-ttu-id="bc576-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc576-118">Requirement</span></span> | <span data-ttu-id="bc576-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bc576-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc576-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc576-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc576-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc576-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc576-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc576-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc576-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bc576-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bc576-124">Header</span><span class="sxs-lookup"><span data-stu-id="bc576-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc576-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bc576-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bc576-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bc576-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc576-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc576-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bc576-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc576-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc576-129">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="bc576-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="bc576-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="bc576-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bc576-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="bc576-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="bc576-132">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="bc576-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="bc576-133">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="bc576-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="bc576-134">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="bc576-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="bc576-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="bc576-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




