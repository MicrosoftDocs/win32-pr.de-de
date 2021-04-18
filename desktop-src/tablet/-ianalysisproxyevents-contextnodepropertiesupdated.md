---
description: Tritt auf, nachdem der iinkanalyzer eine oder mehrere Eigenschaften eines icontextnode-Objekts aktualisiert hat.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: '_IAnalysisProxyEvents:: contextnodebug-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365238"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="2e176-103">\_Ianalysisproxyevents:: contextnodebug-Ereignis</span><span class="sxs-lookup"><span data-stu-id="2e176-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="2e176-104">Tritt auf, nachdem der [**iinkanalyzer**](iinkanalyzer.md) eine oder mehrere Eigenschaften eines [**icontextnode**](icontextnode.md) -Objekts aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="2e176-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e176-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e176-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="2e176-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e176-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e176-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e176-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e176-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das die Eigenschaften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2e176-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="2e176-109">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e176-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e176-110">Das [**icontextnode**](icontextnode.md) -Objekt, dessen Eigenschaften aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2e176-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e176-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e176-111">Return value</span></span>

<span data-ttu-id="2e176-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2e176-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e176-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e176-113">Remarks</span></span>

<span data-ttu-id="2e176-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2e176-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="2e176-115">Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die die Eigenschaften eines [**icontextnode**](icontextnode.md) ändert (siehe [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="2e176-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="2e176-116">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2e176-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e176-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e176-117">Requirements</span></span>



| <span data-ttu-id="2e176-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e176-118">Requirement</span></span> | <span data-ttu-id="2e176-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2e176-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e176-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e176-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e176-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e176-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e176-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e176-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e176-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2e176-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2e176-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e176-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e176-125"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e176-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e176-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2e176-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e176-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e176-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2e176-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e176-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e176-129">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="2e176-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="2e176-130">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="2e176-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2e176-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="2e176-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2e176-132">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="2e176-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2e176-133">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="2e176-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2e176-134">Kontext Knoten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e176-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="2e176-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="2e176-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




