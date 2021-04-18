---
description: Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für mehrere Striche hinzu.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Iinkanalyzer:: addstrokestocustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347780"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="dfdbd-103">Iinkanalyzer:: addstrokestocustomerkenzer-Methode</span><span class="sxs-lookup"><span data-stu-id="dfdbd-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="dfdbd-104">Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für mehrere Striche hinzu.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdbd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfdbd-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="dfdbd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfdbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfdbd-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-108">Die Anzahl der hinzu zufügenden Striche.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-110">Ein Array, das die Strich Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-111">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-112">Die Anzahl der Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-113">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-114">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-115">*pulpacketdatacountperstroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-116">Ein Array, das die Anzahl der Pakete in jedem Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-117">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-118">Ein Array, das die Paketdaten für die Striche enthält.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-119">*pcustomerkenzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-120">Der [**icontextnode**](icontextnode.md) des Typs **customerkenzer** , dem die Striche hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="dfdbd-121">*ppcontextnodestrokeaddto* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfdbd-122">Der [**icontextnode**](icontextnode.md) , dem die Handschrift Analyse die Striche hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfdbd-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfdbd-123">Return value</span></span>

<span data-ttu-id="dfdbd-124">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dfdbd-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfdbd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfdbd-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dfdbd-126">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="dfdbd-127">Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="dfdbd-128">Der [**iinkanalyzer**](iinkanalyzer.md) fügt die Striche einem [**icontextnode**](icontextnode.md) des Typs **customerkenzer** hinzu (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="dfdbd-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="dfdbd-129">Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="dfdbd-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="dfdbd-130">[**Iinkanalyzer**](iinkanalyzer.md) weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu und fügt die Striche dem ersten Knoten **unclassimeedink** unter dem Knoten **customerkenzer** hinzu.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="dfdbd-131">Wenn kein **unclassimeedink** -Knoten vorhanden ist, wird er erstellt.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="dfdbd-132">Wenn das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das dem **customerkenzer** -Knoten zugeordnet ist, den Kultur Bezeichner nicht unterstützt, setzt **iinkanalyzer** die Analyse fort und generiert eine [**ianalysiswarning**](ianalysiswarning.md) -Warnung.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="dfdbd-133">Diese Warnung weist einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ LanguageIdNotRespected** auf.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="dfdbd-134">*plstrokepacketdata* enthält Paketdaten für alle Striche.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="dfdbd-135">*pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="dfdbd-136">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="dfdbd-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="dfdbd-137">Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen **iinkanalyzer:: addstrokestocustomerkenzer-Methoden** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="dfdbd-138">Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld der hinzugefügten Striche erweitert.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="dfdbd-139">Der [**iinkanalyzer**](iinkanalyzer.md) gibt unter den folgenden Umständen ein **HRESULT** von **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="dfdbd-140">Der [**iinkanalyzer**](iinkanalyzer.md) enthält bereits einen Strich mit dem gleichen Bezeichner wie einen der hinzu zufügenden Striche.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="dfdbd-141">Der *pcustomerkenzer* -Parameter enthält einen benutzerdefinierten Erkennungs Knoten, der mit einem anderen [**iinkanalyzer**](iinkanalyzer.md) -Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="dfdbd-142">Der *pcustomerkenzer* -Parameter enthält einen [**icontextnode**](icontextnode.md) , der nicht vom Typ " **customerkenzer**" ist.</span><span class="sxs-lookup"><span data-stu-id="dfdbd-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfdbd-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfdbd-143">Requirements</span></span>



| <span data-ttu-id="dfdbd-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfdbd-144">Requirement</span></span> | <span data-ttu-id="dfdbd-145">Wert</span><span class="sxs-lookup"><span data-stu-id="dfdbd-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfdbd-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfdbd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="dfdbd-147">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfdbd-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dfdbd-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfdbd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="dfdbd-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dfdbd-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dfdbd-150">Header</span><span class="sxs-lookup"><span data-stu-id="dfdbd-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfdbd-151"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dfdbd-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dfdbd-152">DLL</span><span class="sxs-lookup"><span data-stu-id="dfdbd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfdbd-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfdbd-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dfdbd-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfdbd-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfdbd-155">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="dfdbd-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dfdbd-156">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="dfdbd-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="dfdbd-157">**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="dfdbd-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="dfdbd-158">**Iinkanalyzer:: kreatecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="dfdbd-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="dfdbd-159">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="dfdbd-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

