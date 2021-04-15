---
description: Lädt gespeicherte Analyseergebnisse in iinkanalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Iinkanalyzer:: loadresults-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485075"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="90114-103">Iinkanalyzer:: loadresults-Methode</span><span class="sxs-lookup"><span data-stu-id="90114-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="90114-104">Lädt gespeicherte Analyseergebnisse in [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="90114-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90114-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90114-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="90114-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="90114-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90114-107">*uldatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90114-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-108">Die Anzahl von Bytes in *pbserializedresults*.</span><span class="sxs-lookup"><span data-stu-id="90114-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="90114-109">*pbserializedresults* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90114-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-110">Die serialisierten Analyseergebnisse.</span><span class="sxs-lookup"><span data-stu-id="90114-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="90114-111">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90114-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-112">Die Anzahl der Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="90114-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="90114-113">*ploriginalstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90114-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-114">Das Array der ursprünglichen Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="90114-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="90114-115">*plnewstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90114-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-116">Das Array neuer Strich Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="90114-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="90114-117">*pferfolgreich* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="90114-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="90114-118">**Variant \_ TRUE** , wenn das Laden erfolgreich war. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="90114-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90114-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90114-119">Return value</span></span>

<span data-ttu-id="90114-120">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="90114-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="90114-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90114-121">Remarks</span></span>

<span data-ttu-id="90114-122">Wenn [**iinkanalyzer**](iinkanalyzer.md) aus den gespeicherten Ergebnissen einen [**icontextnode**](icontextnode.md) hinzufügt, wird dem **icontextnode** eine neue Globally Unique Identifier (GUID) zugewiesen (siehe [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md) und [Kontext Knoten Eigenschaften](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="90114-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="90114-123">Mit dieser Methode werden die gespeicherten Analyseergebnisse der vorhandenen [**icontextnode**](icontextnode.md) -Struktur hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="90114-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="90114-124">Um sicherzustellen, dass die kombinierten Ergebnisse ordnungsgemäß geordnet sind, fügen Sie den Bereich mit den geladenen Kontext Knoten dem geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzu (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)), und analysieren Sie die frei Hand Eingaben erneut.</span><span class="sxs-lookup"><span data-stu-id="90114-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="90114-125">Die Methoden Methoden [**iinkanalyzer:: SaveResults**](iinkanalyzer-saveresults.md), [**iinkanalyzer:: saveresultsfornodes**](iinkanalyzer-saveresultsfornodes.md)und [**iinkanalyzer:: saveresultsforstriche**](iinkanalyzer-saveresultsforstrokes.md) speichern die Paketdaten nicht zusammen mit den Analyseergebnissen.</span><span class="sxs-lookup"><span data-stu-id="90114-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="90114-126">Jeder Bezeichner in *ploriginalstrokeids* ist der Strich Bezeichner für den Strich in den gespeicherten Analyseergebnissen.</span><span class="sxs-lookup"><span data-stu-id="90114-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="90114-127">Jeder Bezeichner in *plnewstrokeids* ist der neue Bezeichner, mit dem der ursprüngliche Bezeichner in den geladenen Analyseergebnissen ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90114-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="90114-128">Wenn ein gespeicherter Analyse Hinweis einen Konflikt mit einem vorhandenen Analyse Hinweis verursacht, lädt der [**iinkanalyzer**](iinkanalyzer.md) den gespeicherten Hinweis nicht, lädt jedoch die restlichen gespeicherten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="90114-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="90114-129">Wenn jedoch **iinkanalyzer** Ergebnisse für einen Strich lädt, der sich innerhalb des Bereichs eines gespeicherten Analyse Hinweises befindet, dass der **iinkanalyzer** nicht geladen wird, fügt **iinkanalyzer** das umgebende Feld des Strichs dem geänderten Bereich des **iinkanalyzer** -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="90114-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="90114-130">Wenn **iinkanalyzer** Ergebnisse für einen Strich lädt, der sich innerhalb eines vorhandenen Analyse Hinweises befindet, fügt der **iinkanalyzer** auch das umgebende Feld des Strichs dem geänderten Bereich des **iinkanalyzer** -Objekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="90114-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="90114-131">Weitere Informationen zu Analyse hinweisen finden Sie unter [Eigenschaften des Analysis-Hinweises](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="90114-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="90114-132">Diese Methode kann die Ereignisse [**\_ ianalysisproxyevents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ ianalysisproxyevents:: contextnodelta inkadditions**](-ianalysisproxyevents-contextnodelinkadding.md)und [**\_ ianalysisproxyevents:: contextnodepropertiesaktualisierten**](-ianalysisproxyevents-contextnodepropertiesupdated.md) beim Laden der gespeicherten Ergebnisse hervorrufen.</span><span class="sxs-lookup"><span data-stu-id="90114-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="90114-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90114-133">Requirements</span></span>



| <span data-ttu-id="90114-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90114-134">Requirement</span></span> | <span data-ttu-id="90114-135">Wert</span><span class="sxs-lookup"><span data-stu-id="90114-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90114-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90114-136">Minimum supported client</span></span><br/> | <span data-ttu-id="90114-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90114-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="90114-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90114-138">Minimum supported server</span></span><br/> | <span data-ttu-id="90114-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90114-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="90114-140">Header</span><span class="sxs-lookup"><span data-stu-id="90114-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="90114-141"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="90114-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="90114-142">DLL</span><span class="sxs-lookup"><span data-stu-id="90114-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90114-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90114-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="90114-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90114-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90114-145">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="90114-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="90114-146">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="90114-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="90114-147">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="90114-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="90114-148">**Iinkanalyzer:: setdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="90114-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="90114-149">**Iinkanalyzer:: SaveResults-Methode**</span><span class="sxs-lookup"><span data-stu-id="90114-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="90114-150">**Iinkanalyzer:: saveresultsfornodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="90114-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="90114-151">**Iinkanalyzer:: saveresultsforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="90114-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="90114-152">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="90114-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




