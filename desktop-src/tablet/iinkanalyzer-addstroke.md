---
description: Fügt dem iinkanalyzer Strich Daten für einen einzelnen Strich hinzu und weist dem Strich den Kultur Bezeichner des aktiven Eingabe Threads zu.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'Iinkanalyzer:: AddStroke-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214668"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="a3de6-103">Iinkanalyzer:: AddStroke-Methode</span><span class="sxs-lookup"><span data-stu-id="a3de6-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="a3de6-104">Fügt dem [**iinkanalyzer**](iinkanalyzer.md) Strich Daten für einen einzelnen Strich hinzu und weist dem Strich den Kultur Bezeichner des aktiven Eingabe Threads zu.</span><span class="sxs-lookup"><span data-stu-id="a3de6-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3de6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3de6-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="a3de6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3de6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3de6-107">*lstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-108">Der Bezeichner für den hinzu zufügenden Strich.</span><span class="sxs-lookup"><span data-stu-id="a3de6-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="a3de6-109">*ulstrokepacketdatacount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-110">Die Anzahl der Pakete im Strich.</span><span class="sxs-lookup"><span data-stu-id="a3de6-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a3de6-111">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-112">Ein Array, das die Paketdaten für den Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="a3de6-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a3de6-113">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-114">Die Anzahl der Paket Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="a3de6-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="a3de6-115">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-116">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="a3de6-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a3de6-117">*ppcontextnodestrokeaddto* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3de6-118">Ein Zeiger auf den [**icontextnode**](icontextnode.md) , dem [**iinkanalyzer**](iinkanalyzer.md) den Strich hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="a3de6-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3de6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3de6-119">Return value</span></span>

<span data-ttu-id="a3de6-120">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a3de6-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3de6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3de6-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a3de6-122">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a3de6-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a3de6-123">Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3de6-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="a3de6-124">[**Iinkanalyzer**](iinkanalyzer.md) fügt den Strich einem [**icontextnode**](icontextnode.md) vom Typ UnclassifiedInk hinzu (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="a3de6-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="a3de6-125">Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="a3de6-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="a3de6-126">[**Iinkanalyzer**](iinkanalyzer.md) weist den Kultur Bezeichner des aktiven Eingabe Threads dem Strich zu und fügt den Strich dem ersten UnclassifiedInk-Kontext Knoten unter dem Stamm Knoten der Ink Analyzer hinzu, der Striche mit dem gleichen Kultur Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="a3de6-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="a3de6-127">Wenn der Ink Analyzer keinen Knoten mit demselben Kultur Bezeichner besitzt, erstellt er einen neuen UnclassifiedInk-Kontext Knoten unter seinem Stamm Knoten und fügt den Strich dem neuen UnclassifiedInk-Kontext Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3de6-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="a3de6-128">*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich.</span><span class="sxs-lookup"><span data-stu-id="a3de6-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="a3de6-129">*pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt im Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a3de6-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="a3de6-130">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a3de6-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="a3de6-131">Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld des hinzugefügten Strichs erweitert.</span><span class="sxs-lookup"><span data-stu-id="a3de6-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="a3de6-132">Wenn [**iinkanalyzer**](iinkanalyzer.md) bereits einen Strich mit dem gleichen Strich Bezeichner enthält, gibt **iinkanalyzer** ein **HRESULT** von **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="a3de6-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3de6-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3de6-133">Requirements</span></span>



| <span data-ttu-id="a3de6-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3de6-134">Requirement</span></span> | <span data-ttu-id="a3de6-135">Wert</span><span class="sxs-lookup"><span data-stu-id="a3de6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3de6-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3de6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a3de6-137">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3de6-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a3de6-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3de6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a3de6-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a3de6-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a3de6-140">Header</span><span class="sxs-lookup"><span data-stu-id="a3de6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3de6-141"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a3de6-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a3de6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a3de6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3de6-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3de6-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a3de6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3de6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3de6-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a3de6-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a3de6-146">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a3de6-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a3de6-147">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="a3de6-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a3de6-148">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a3de6-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a3de6-149">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="a3de6-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="a3de6-150">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="a3de6-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="a3de6-151">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a3de6-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

