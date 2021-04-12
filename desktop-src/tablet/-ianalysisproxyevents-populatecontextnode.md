---
description: Tritt auf, bevor der iinkanalyzer innerhalb des Bereichs eines teilweise aufgefüllten icontextnode-Objekts eine Analyse ausführt.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P-Ereignis "opulatecontextnode" (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219056"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="6af43-103">\_Ianalysisproxyevents::P opulatecontextnode-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6af43-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="6af43-104">Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) innerhalb des Bereichs eines teilweise aufgefüllten [**icontextnode**](icontextnode.md) -Objekts eine Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="6af43-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6af43-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="6af43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6af43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af43-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af43-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af43-108">Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das eine Analyse durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="6af43-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="6af43-109">*pcontextnodebug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6af43-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af43-110">Das teilweise aufgefüllte [**icontextnode**](icontextnode.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6af43-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af43-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6af43-111">Return value</span></span>

<span data-ttu-id="6af43-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6af43-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6af43-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6af43-113">Remarks</span></span>

<span data-ttu-id="6af43-114">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6af43-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="6af43-115">Wenn das **iinkanalyzer** -Ereignis dieses Ereignis auslöst, sollte die Anwendung *pcontextnodebug (pcontextnodebug*) auffüllen.</span><span class="sxs-lookup"><span data-stu-id="6af43-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="6af43-116">Während der Analysephase löst **iinkanalyzer** dieses Ereignis aus, um Informationen für die Bereiche zu erhalten, in denen frei Hand Eingaben analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="6af43-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="6af43-117">Wenn das Dokument Links für die *pcontextnodebug-topopulate* enthält, sollte Ihre Anwendung diese Links erstellen und hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6af43-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="6af43-118">Dieser Prozess erfordert, dass sowohl der Quell-als auch der Zielknoten (einschließlich seiner Vorgänger) vollständig aufgefüllt werden, bevor der Ereignishandler für dieses Ereignis beendet wird (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md) und [**icontextlink:: getdestinationnode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="6af43-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="6af43-119">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6af43-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="6af43-120">Während der Hintergrundanalyse löst das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis dieses Ereignis aus, nachdem es das [**\_ ianalysisevents:: leserytoricile**](-ianalysisevents-readytoreconcile.md) -Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="6af43-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af43-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6af43-121">Requirements</span></span>



| <span data-ttu-id="6af43-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6af43-122">Requirement</span></span> | <span data-ttu-id="6af43-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6af43-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af43-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6af43-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6af43-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6af43-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6af43-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6af43-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6af43-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6af43-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6af43-128">Header</span><span class="sxs-lookup"><span data-stu-id="6af43-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af43-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6af43-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6af43-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6af43-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6af43-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af43-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6af43-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6af43-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af43-133">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="6af43-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="6af43-134">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="6af43-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6af43-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="6af43-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6af43-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="6af43-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="6af43-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="6af43-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="6af43-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="6af43-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




