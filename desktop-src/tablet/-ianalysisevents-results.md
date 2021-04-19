---
description: Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents:: results-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355112"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="05f57-103">\_Ianalysil Vents:: results-Ereignis</span><span class="sxs-lookup"><span data-stu-id="05f57-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="05f57-104">Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="05f57-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05f57-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="05f57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05f57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f57-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05f57-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f57-108">Der [**iinkanalyzer**](iinkanalyzer.md) , der die Analyseergebnisse erzeugt.</span><span class="sxs-lookup"><span data-stu-id="05f57-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="05f57-109">*panalysisstatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05f57-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f57-110">Das [**ianalysisstatus**](ianalysisstatus.md) -Objekt, das den Status der Analyse darstellt.</span><span class="sxs-lookup"><span data-stu-id="05f57-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f57-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05f57-111">Return value</span></span>

<span data-ttu-id="05f57-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="05f57-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05f57-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05f57-113">Remarks</span></span>

<span data-ttu-id="05f57-114">Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es die Ergebnisse für die abschließende Analysephase abgestimmt hat.</span><span class="sxs-lookup"><span data-stu-id="05f57-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="05f57-115">Wenn Ihre Anwendung die [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)aufruft, signalisiert dieses Ereignis, wann die Analyseergebnisse bereit sind.</span><span class="sxs-lookup"><span data-stu-id="05f57-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="05f57-116">Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird, weist dieses Ereignis darauf hin, dass der **iinkanalyzer** seine internen Daten für diese Analysephase geändert hat.</span><span class="sxs-lookup"><span data-stu-id="05f57-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="05f57-117">Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="05f57-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="05f57-118">Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="05f57-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="05f57-119">Entsperren Sie Ihre Datenstruktur, wenn **iinkanalyzer** das [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -oder **\_ ianalysilvents:: results** -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="05f57-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="05f57-120">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="05f57-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05f57-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05f57-121">Requirements</span></span>



| <span data-ttu-id="05f57-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05f57-122">Requirement</span></span> | <span data-ttu-id="05f57-123">Wert</span><span class="sxs-lookup"><span data-stu-id="05f57-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f57-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05f57-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05f57-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05f57-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="05f57-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05f57-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05f57-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05f57-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="05f57-128">Header</span><span class="sxs-lookup"><span data-stu-id="05f57-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f57-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="05f57-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="05f57-130">DLL</span><span class="sxs-lookup"><span data-stu-id="05f57-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f57-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f57-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="05f57-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05f57-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f57-133">**\_Ianalysil Vents**</span><span class="sxs-lookup"><span data-stu-id="05f57-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="05f57-134">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="05f57-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="05f57-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="05f57-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="05f57-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="05f57-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="05f57-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="05f57-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="05f57-138">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="05f57-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="05f57-139">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="05f57-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




