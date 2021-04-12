---
description: Gibt an, wie iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: AnalysisModes-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393238"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="7197e-103">AnalysisModes-Enumeration</span><span class="sxs-lookup"><span data-stu-id="7197e-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="7197e-104">Gibt an, wie [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="7197e-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7197e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7197e-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="7197e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="7197e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7197e-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ None**</span><span class="sxs-lookup"><span data-stu-id="7197e-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="7197e-108">Es wurden keine Modi angegeben.</span><span class="sxs-lookup"><span data-stu-id="7197e-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="7197e-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ automatikreversöhnung**</span><span class="sxs-lookup"><span data-stu-id="7197e-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="7197e-110">Gibt an, ob der [**iinkanalyzer**](iinkanalyzer.md) den Abstimmungs Vorgang automatisch startet, sobald die Zwischenergebnisse oder Endergebnisse bereit sind.</span><span class="sxs-lookup"><span data-stu-id="7197e-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="7197e-111">Wenn dieser Modus aktiviert ist, wird das [**\_ ianalysissevents:: leseytor econcile**](-ianalysisevents-readytoreconcile.md) -Ereignis nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7197e-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="7197e-112">Wenn dieser Modus deaktiviert ist, wird das **\_ ianalysissevents:: leseytor econcile** -Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7197e-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="7197e-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ strokecacheautocleanup**</span><span class="sxs-lookup"><span data-stu-id="7197e-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="7197e-114">Gibt an, ob der [**iinkanalyzer**](iinkanalyzer.md) automatisch nicht benötigte Striche aus dem Strich Cache löscht, bevor eine Analyse durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7197e-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="7197e-115">Wenn dieser Modus aktiviert ist, löscht [**iinkanalyzer**](iinkanalyzer.md) die Strich Daten vor dem Durchführen der Analyse.</span><span class="sxs-lookup"><span data-stu-id="7197e-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="7197e-116">Der Code muss dann auch das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="7197e-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="7197e-117">Wenn das **\_ ianalysil Vents:: updatestrokescache** -Ereignis nicht behandelt wird, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7197e-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="7197e-118">Diese Überprüfung erfolgt sowohl bei den Analyse-(oder BackgroundAnalyze)-als auch bei Abstimmungs Phasen.</span><span class="sxs-lookup"><span data-stu-id="7197e-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="7197e-119">Wenn dieser Modus deaktiviert ist, werden die Strich Daten von [**iinkanalyzer**](iinkanalyzer.md) nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7197e-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="7197e-120">Um die Strich Daten zu löschen, müssen Sie die [**iinkanalyzer:: ClearStrokeData-Methode**](iinkanalyzer-clearstrokedata.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7197e-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="7197e-121">Wenn dieser Modus deaktiviert ist, wird das [**\_ ianalysitsvents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis ausgelöst, sodass der **iinkanalyzer** die neuesten hubdaten für alle Striche abrufen kann, bei denen der Cache gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="7197e-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="7197e-122">Wenn der Strich Cache gelöscht wird, das **\_ ianalysil Vents:: updatestrokescache** -Ereignis jedoch nicht behandelt wird, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7197e-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="7197e-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ personalizationaktivierte**</span><span class="sxs-lookup"><span data-stu-id="7197e-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="7197e-124">Die Personalisierung der Handschrifterkennung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7197e-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7197e-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes ( \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="7197e-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="7197e-126">Alle Modi sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7197e-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7197e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7197e-127">Remarks</span></span>

<span data-ttu-id="7197e-128">Diese Enumeration ermöglicht eine bitweise Kombination der Element Werte.</span><span class="sxs-lookup"><span data-stu-id="7197e-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7197e-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7197e-129">Requirements</span></span>



| <span data-ttu-id="7197e-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7197e-130">Requirement</span></span> | <span data-ttu-id="7197e-131">Wert</span><span class="sxs-lookup"><span data-stu-id="7197e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7197e-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7197e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7197e-133">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7197e-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7197e-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7197e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7197e-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7197e-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7197e-136">Header</span><span class="sxs-lookup"><span data-stu-id="7197e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7197e-137"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7197e-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7197e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7197e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7197e-139">**Iinkanalyzer:: getanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="7197e-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7197e-140">**Iinkanalyzer:: abtanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="7197e-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7197e-141">**\_Ianalysilvents:: IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="7197e-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="7197e-142">**\_Ianalysissevents:: luytor econcile**</span><span class="sxs-lookup"><span data-stu-id="7197e-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="7197e-143">**\_Ianalysil Vents:: updatestrokescache**</span><span class="sxs-lookup"><span data-stu-id="7197e-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="7197e-144">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="7197e-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




