---
description: Fügt dem iinkanalyzer Strich Daten für mehrere Striche hinzu und weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Iinkanalyzer:: AddStrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348194"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="15287-103">Iinkanalyzer:: AddStrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="15287-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="15287-104">Fügt dem [**iinkanalyzer**](iinkanalyzer.md) Strich Daten für mehrere Striche hinzu und weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu.</span><span class="sxs-lookup"><span data-stu-id="15287-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="15287-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15287-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="15287-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15287-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-108">Die Anzahl der hinzu zufügenden Striche.</span><span class="sxs-lookup"><span data-stu-id="15287-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="15287-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-110">Ein Array, das die Strich Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="15287-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="15287-111">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-112">Die Anzahl der Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="15287-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="15287-113">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-114">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="15287-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="15287-115">*pulpacketdatacountperstroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-116">Ein Array, das die Anzahl der Pakete in jedem Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="15287-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="15287-117">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15287-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-118">Ein Array, das die Paketdaten für die Striche enthält.</span><span class="sxs-lookup"><span data-stu-id="15287-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="15287-119">*ppcontextnodestrokeaddto* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="15287-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15287-120">Der [**icontextnode**](icontextnode.md) , dem die Handschrift Analyse die Striche hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="15287-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15287-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15287-121">Return value</span></span>

<span data-ttu-id="15287-122">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="15287-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15287-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15287-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="15287-124">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="15287-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="15287-125">Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="15287-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="15287-126">Der [**iinkanalyzer**](iinkanalyzer.md) fügt die Striche einem [**icontextnode**](icontextnode.md) vom Typ unclassimeedink hinzu (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="15287-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="15287-127">Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="15287-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="15287-128">[**Iinkanalyzer**](iinkanalyzer.md) weist den Strichen den Kultur Bezeichner des aktiven Eingabe Threads zu und fügt die Striche dem ersten unclassi\edink-Kontext Knoten unter dem Stamm Knoten der Ink Analyzer hinzu, der Striche mit dem gleichen Kultur Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="15287-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="15287-129">Wenn der Ink Analyzer keinen Knoten mit demselben Kultur Bezeichner besitzt, erstellt er einen neuen unclassimeedink-Kontext Knoten unter seinem Stamm Knoten und fügt die Striche dem neuen unclassi\edink-Kontext Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="15287-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="15287-130">*plstrokepacketdata* enthält Paketdaten für alle Striche.</span><span class="sxs-lookup"><span data-stu-id="15287-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="15287-131">*pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="15287-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="15287-132">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="15287-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="15287-133">Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen **iinkanalyzer:: AddStrokes-Methoden** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="15287-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="15287-134">Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld der hinzugefügten Striche erweitert.</span><span class="sxs-lookup"><span data-stu-id="15287-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="15287-135">Wenn [**iinkanalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Bezeichner wie einen der hinzu zufügenden Striche enthält, gibt **iinkanalyzer** ein **HRESULT** von **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="15287-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15287-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15287-136">Requirements</span></span>



| <span data-ttu-id="15287-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15287-137">Requirement</span></span> | <span data-ttu-id="15287-138">Wert</span><span class="sxs-lookup"><span data-stu-id="15287-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15287-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15287-139">Minimum supported client</span></span><br/> | <span data-ttu-id="15287-140">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15287-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15287-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15287-141">Minimum supported server</span></span><br/> | <span data-ttu-id="15287-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15287-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="15287-143">Header</span><span class="sxs-lookup"><span data-stu-id="15287-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="15287-144"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15287-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15287-145">DLL</span><span class="sxs-lookup"><span data-stu-id="15287-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15287-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15287-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="15287-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15287-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15287-148">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="15287-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="15287-149">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="15287-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="15287-150">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="15287-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="15287-151">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="15287-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="15287-152">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="15287-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="15287-153">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="15287-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="15287-154">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="15287-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

