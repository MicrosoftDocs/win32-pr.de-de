---
description: Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für einen einzelnen Strich hinzu.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Iinkanalyzer:: addstrokedecustomerkenzer-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348794"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="b4c03-103">Iinkanalyzer:: addstrokedecustomerkenzer-Methode</span><span class="sxs-lookup"><span data-stu-id="b4c03-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="b4c03-104">Fügt einem benutzerdefinierten Erkennungs Knoten Strich Daten für einen einzelnen Strich hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4c03-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4c03-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="b4c03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c03-107">*ulstrokeid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-108">Der Bezeichner für den hinzu zufügenden Strich.</span><span class="sxs-lookup"><span data-stu-id="b4c03-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-109">*ulstrokepacketdatacount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-110">Die Anzahl der Pakete im Strich.</span><span class="sxs-lookup"><span data-stu-id="b4c03-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-111">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-112">Ein Array, das die Paketdaten für den Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="b4c03-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-113">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-114">Die Anzahl der Paket Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="b4c03-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-115">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-116">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="b4c03-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-117">*pcustomerkenzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-118">Der [**icontextnode**](icontextnode.md) des Typs **customerkenzer** , dem der Strich hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4c03-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="b4c03-119">*ppcontextnodestrokeaddto* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c03-120">Der [**icontextnode**](icontextnode.md) , dem die Ink-Analyse den Strich hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="b4c03-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c03-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4c03-121">Return value</span></span>

<span data-ttu-id="b4c03-122">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b4c03-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c03-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4c03-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b4c03-124">Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnozerstörkeaddto* abrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="b4c03-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b4c03-125">Wenn *ppcontextnodestrokeaddedto* **null** ist, gibt es an, dass der Aufrufer nicht an dem Rückgabewert der-Methode interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4c03-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="b4c03-126">[**Iinkanalyzer**](iinkanalyzer.md) fügt den Strich einem [**icontextnode**](icontextnode.md) des Typs **customerkenzer** hinzu (siehe [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="b4c03-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="b4c03-127">Dieser Knoten befindet sich in der unter Knoten Sammlung des Stamm Knotens (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) -Methoden).</span><span class="sxs-lookup"><span data-stu-id="b4c03-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="b4c03-128">[**Iinkanalyzer**](iinkanalyzer.md) weist den Kultur Bezeichner des aktiven Eingabe Threads dem Strich zu und fügt den Strich dem ersten Knoten **UnclassifiedInk** unter dem Knoten **customerkenzer** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4c03-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="b4c03-129">Wenn kein **unclassimeedink** -Knoten vorhanden ist, wird er erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4c03-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="b4c03-130">Wenn das [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Element, das dem **customerkenzer** -Knoten zugeordnet ist, den Kultur Bezeichner nicht unterstützt, setzt **iinkanalyzer** die Analyse fort und generiert eine [**ianalysiswarning**](ianalysiswarning.md) -Warnung.</span><span class="sxs-lookup"><span data-stu-id="b4c03-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="b4c03-131">Diese Warnung weist einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ LanguageIdNotRespected** auf.</span><span class="sxs-lookup"><span data-stu-id="b4c03-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="b4c03-132">*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich.</span><span class="sxs-lookup"><span data-stu-id="b4c03-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="b4c03-133">*pstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4c03-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="b4c03-134">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b4c03-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="b4c03-135">Mit dieser Methode wird der geänderte Bereich in die Gesamtmenge des aktuellen Werts des Bereichs und das umgebende Feld des hinzugefügten Strichs erweitert.</span><span class="sxs-lookup"><span data-stu-id="b4c03-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="b4c03-136">Der [**iinkanalyzer**](iinkanalyzer.md) gibt unter den folgenden Umständen ein **HRESULT** von **E \_ invalidArg** zurück.</span><span class="sxs-lookup"><span data-stu-id="b4c03-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="b4c03-137">Der [**iinkanalyzer**](iinkanalyzer.md) enthält bereits einen Strich mit dem gleichen Bezeichner wie der hinzu zufügende Strich.</span><span class="sxs-lookup"><span data-stu-id="b4c03-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="b4c03-138">Der *pcustomerkenzer* -Parameter enthält einen benutzerdefinierten Erkennungs Knoten, der mit einem anderen [**iinkanalyzer**](iinkanalyzer.md) -Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="b4c03-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="b4c03-139">Der *pcustomerkenzer* -Parameter enthält einen [**icontextnode**](icontextnode.md) , der nicht vom Typ " **customerkenzer**" ist.</span><span class="sxs-lookup"><span data-stu-id="b4c03-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c03-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4c03-140">Requirements</span></span>



| <span data-ttu-id="b4c03-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4c03-141">Requirement</span></span> | <span data-ttu-id="b4c03-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b4c03-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c03-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4c03-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c03-144">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4c03-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4c03-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4c03-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c03-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4c03-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4c03-147">Header</span><span class="sxs-lookup"><span data-stu-id="b4c03-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c03-148"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4c03-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4c03-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b4c03-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4c03-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4c03-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4c03-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4c03-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c03-152">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="b4c03-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b4c03-153">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="b4c03-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="b4c03-154">**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4c03-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b4c03-155">**Iinkanalyzer:: kreatecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4c03-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b4c03-156">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b4c03-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

