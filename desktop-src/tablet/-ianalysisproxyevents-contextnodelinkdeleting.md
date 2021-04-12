---
description: Tritt auf, bevor iinkanalyzer ein icontextlink-Objekt zwischen zwei icontextnode-Objekten löscht.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: '_IAnalysisProxyEvents:: contextnodelinklösch-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219047"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="fcea9-103">\_Ianalysisproxyevents:: contextnodelinklösch-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fcea9-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="fcea9-104">Tritt auf, bevor [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten löscht.</span><span class="sxs-lookup"><span data-stu-id="fcea9-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcea9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcea9-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="fcea9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcea9-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcea9-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcea9-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Element, das den Link löscht.</span><span class="sxs-lookup"><span data-stu-id="fcea9-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="fcea9-109">*pcontextlinkumbedeleted* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcea9-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcea9-110">Das [**icontextlink**](icontextlink.md) -Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcea9-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcea9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcea9-111">Return value</span></span>

<span data-ttu-id="fcea9-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fcea9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fcea9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcea9-113">Remarks</span></span>

<span data-ttu-id="fcea9-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="fcea9-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="fcea9-115">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine **iinkanalyzer** -Methode auf, die einen [**icontextlink**](icontextlink.md) aus einem [**icontextnode**](icontextnode.md)entfernt.</span><span class="sxs-lookup"><span data-stu-id="fcea9-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="fcea9-116">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fcea9-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcea9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcea9-117">Requirements</span></span>



| <span data-ttu-id="fcea9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcea9-118">Requirement</span></span> | <span data-ttu-id="fcea9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fcea9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcea9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcea9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcea9-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcea9-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fcea9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcea9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcea9-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fcea9-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fcea9-124">Header</span><span class="sxs-lookup"><span data-stu-id="fcea9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcea9-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fcea9-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fcea9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fcea9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcea9-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcea9-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fcea9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcea9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcea9-129">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="fcea9-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="fcea9-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="fcea9-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fcea9-131">**Icontextlink**</span><span class="sxs-lookup"><span data-stu-id="fcea9-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="fcea9-132">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="fcea9-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fcea9-133">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="fcea9-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fcea9-134">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="fcea9-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fcea9-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="fcea9-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




