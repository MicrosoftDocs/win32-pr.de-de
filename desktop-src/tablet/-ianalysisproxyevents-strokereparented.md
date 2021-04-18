---
description: Tritt auf, wenn der iinkanalyzer einen Strich von einem icontextnode-Objekt zu einem anderen verschiebt.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents:: strokereparame-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361130"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="474b4-103">\_Ianalysisproxyevents:: strokereproented-Ereignis</span><span class="sxs-lookup"><span data-stu-id="474b4-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="474b4-104">Tritt auf, wenn der [**iinkanalyzer**](iinkanalyzer.md) einen Strich von einem [**icontextnode**](icontextnode.md) -Objekt zu einem anderen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="474b4-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="474b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="474b4-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="474b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="474b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="474b4-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="474b4-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474b4-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das den Strich verschiebt.</span><span class="sxs-lookup"><span data-stu-id="474b4-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="474b4-109">*lstrokeidtomove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="474b4-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474b4-110">Der Bezeichner des zu verschiebenden Strichs.</span><span class="sxs-lookup"><span data-stu-id="474b4-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="474b4-111">*psourcecontextnode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="474b4-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474b4-112">Das [**icontextnode**](icontextnode.md) -Objekt, aus dem der Strich verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="474b4-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="474b4-113">*pdestinationcontextnode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="474b4-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="474b4-114">Das [**icontextnode**](icontextnode.md) -Objekt, in das der Strich verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="474b4-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="474b4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="474b4-115">Return value</span></span>

<span data-ttu-id="474b4-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="474b4-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="474b4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="474b4-117">Remarks</span></span>

<span data-ttu-id="474b4-118">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="474b4-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="474b4-119">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine **iinkanalyzer** -Methode auf, die Strich Daten von einem [**icontextnode**](icontextnode.md) zu einem anderen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="474b4-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="474b4-120">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="474b4-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="474b4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="474b4-121">Requirements</span></span>



| <span data-ttu-id="474b4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="474b4-122">Requirement</span></span> | <span data-ttu-id="474b4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="474b4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="474b4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="474b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="474b4-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="474b4-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="474b4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="474b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="474b4-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="474b4-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="474b4-128">Header</span><span class="sxs-lookup"><span data-stu-id="474b4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="474b4-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="474b4-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="474b4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="474b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="474b4-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="474b4-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="474b4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="474b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474b4-133">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="474b4-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="474b4-134">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="474b4-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="474b4-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="474b4-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="474b4-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="474b4-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="474b4-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="474b4-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="474b4-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="474b4-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




