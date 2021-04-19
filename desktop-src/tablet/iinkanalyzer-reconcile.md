---
description: 'Wendet die Ergebnisse eines Hintergrund-frei Hand Analyse Vorgangs auf die Kontext Knoten Struktur für die Teile der Struktur an, die seit dem Ansichts Vorgang der iinkanalyzer:: BackgroundAnalyze-Methode nicht von der Anwendung geändert wurden.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Iinkanalyzer:: abgestimmt-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345736"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="b8f3d-103">Iinkanalyzer:: abgestimmt-Methode</span><span class="sxs-lookup"><span data-stu-id="b8f3d-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="b8f3d-104">Wendet die Ergebnisse eines Hintergrund-frei Hand Analyse Vorgangs auf die Kontext Knoten Struktur für die Teile der Struktur an, die seit dem Ansichts Vorgang der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)nicht von der Anwendung geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8f3d-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="b8f3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8f3d-106">Parameters</span></span>

<span data-ttu-id="b8f3d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8f3d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8f3d-108">Return value</span></span>

<span data-ttu-id="b8f3d-109">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8f3d-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f3d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8f3d-110">Remarks</span></span>

<span data-ttu-id="b8f3d-111">Standardmäßig führt [**iinkanalyzer**](iinkanalyzer.md) sofort vor dem Auflösen der [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -und [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignisse eine automatische Abstimmungsphase aus.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="b8f3d-112">Um die automatische Abstimmung zu deaktivieren, löschen Sie das **AnalysisModes-Flag \_ automatikreversöhnung** aus den Analyse Modi von Ink Analyzer (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md) und [**AnalysisModes**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="b8f3d-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="b8f3d-113">Die [**Methode "iinkanalyzer:: BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) " gibt einen Fehler zurück, wenn die automatische Abstimmung deaktiviert ist und die Anwendung das [**\_ ianalysisevents:: Read ytoreconcile**](-ianalysisevents-readytoreconcile.md) -Ereignis nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="b8f3d-114">Die Anwendung muss die **Methode iinkanalyzer::** abgestimmt-Methode aufruft, bevor der [**iinkanalyzer**](iinkanalyzer.md) die Ergebnisse weiterverarbeiten oder die weitere Analyse für die entsprechende Analysephase fortsetzen kann.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="b8f3d-115">Die Anwendung kann Änderungen vornehmen, z. b. das Hinzufügen oder Entfernen von Strichen und das Ändern von Strich Daten in der Kontext Knoten Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts während der Hintergrundanalyse.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="b8f3d-116">Solche Änderungen können Teile der Ergebnisse der Hintergrundanalyse für ungültig erklären.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="b8f3d-117">Diese Methode wendet Analyseergebnisse nur auf die Kontext Knoten Struktur des Analyzers für die Teile der Struktur an, die Ihre Anwendung nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b8f3d-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="b8f3d-118">Diese Methode fügt auch Regionen, die ungültige Analyseergebnisse enthalten, in den geänderten Bereich des **iinkanalyzer** -Objekts ein (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="b8f3d-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="b8f3d-119">Weitere Informationen zur Verwendung von zum Analysieren von frei Hand Eingaben finden Sie unter [Übersicht über](ink-analysis-overview.md)die frei Hand Analyse. [**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="b8f3d-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f3d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8f3d-120">Requirements</span></span>



| <span data-ttu-id="b8f3d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8f3d-121">Requirement</span></span> | <span data-ttu-id="b8f3d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b8f3d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f3d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8f3d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f3d-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8f3d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8f3d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8f3d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f3d-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8f3d-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8f3d-127">Header</span><span class="sxs-lookup"><span data-stu-id="b8f3d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f3d-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8f3d-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8f3d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f3d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f3d-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f3d-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8f3d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8f3d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f3d-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="b8f3d-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b8f3d-133">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="b8f3d-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b8f3d-134">**\_Ianalysissevents:: luytor econcile**</span><span class="sxs-lookup"><span data-stu-id="b8f3d-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="b8f3d-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b8f3d-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




