---
description: Fügt dem iinkanalyzer Strich Daten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kultur Bezeichner zu.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'Iinkanalyzer:: addstrokeforlanguage-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862703"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="ea4ae-103">Iinkanalyzer:: addstrokeforlanguage-Methode</span><span class="sxs-lookup"><span data-stu-id="ea4ae-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="ea4ae-104">Fügt dem [**iinkanalyzer**](iinkanalyzer.md) Strich Daten für einen einzelnen Strich hinzu und weist dem Strich einen bestimmten Kultur Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea4ae-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="ea4ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea4ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4ae-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-108">Der Bezeichner für den hinzu zufügenden Strich.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-109">*lstrokelcid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-110">Der Kultur Bezeichner, der dem Strich zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-111">*ulstrokepacketdatacount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-112">Die Anzahl der Pakete im Strich.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-113">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-114">Ein Array, das die Paketdaten für den Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-115">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-116">Die Anzahl der Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-117">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-118">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ea4ae-119">*ppcontextnodestrokeaddto* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4ae-120">Ein Zeiger, dessen Wert auf den Zeiger des [**icontextnode**](icontextnode.md) festgelegt ist, der den neu hinzugefügten Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4ae-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea4ae-121">Return value</span></span>

<span data-ttu-id="ea4ae-122">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ea4ae-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4ae-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea4ae-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ea4ae-124">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ea4ae-125">Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="ea4ae-126">[**Iinkanalyzer**](iinkanalyzer.md) fügt den Strich einem [**icontextnode**](icontextnode.md) vom Typ UnclassifiedInk hinzu (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="ea4ae-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="ea4ae-127">Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="ea4ae-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="ea4ae-128">[**Iinkanalyzer**](iinkanalyzer.md) weist dem Strich den Kultur Bezeichner *lstrokelcid* zu und fügt den Strich dem ersten UnclassifiedInk-Kontext Knoten unter dem Stamm Knoten der Ink Analyzer hinzu, der Striche mit dem gleichen Kultur Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="ea4ae-129">Wenn der Ink Analyzer keinen Knoten mit demselben Kultur Bezeichner besitzt, erstellt er einen neuen UnclassifiedInk-Kontext Knoten unter seinem Stamm Knoten und fügt den Strich dem neuen UnclassifiedInk-Kontext Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="ea4ae-130">*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="ea4ae-131">*pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt im Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="ea4ae-132">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ea4ae-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="ea4ae-133">Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld des hinzugefügten Strichs erweitert.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="ea4ae-134">Wenn [**iinkanalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Strich Bezeichner enthält, gibt **iinkanalyzer** ein **HRESULT** von **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="ea4ae-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4ae-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea4ae-135">Requirements</span></span>



| <span data-ttu-id="ea4ae-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea4ae-136">Requirement</span></span> | <span data-ttu-id="ea4ae-137">Wert</span><span class="sxs-lookup"><span data-stu-id="ea4ae-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4ae-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea4ae-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4ae-139">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4ae-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ea4ae-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea4ae-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4ae-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea4ae-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ea4ae-142">Header</span><span class="sxs-lookup"><span data-stu-id="ea4ae-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4ae-143"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4ae-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ea4ae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ea4ae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4ae-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea4ae-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ea4ae-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea4ae-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4ae-147">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-148">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-149">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-150">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-151">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-152">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="ea4ae-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="ea4ae-153">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ea4ae-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

