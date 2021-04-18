---
description: Aktualisiert die Paketdaten für die angegebenen Striche.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Iinkanalyzer:: UpdateStrokesData-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343690"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="a17c1-103">Iinkanalyzer:: UpdateStrokesData-Methode</span><span class="sxs-lookup"><span data-stu-id="a17c1-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="a17c1-104">Aktualisiert die Paketdaten für die angegebenen Striche.</span><span class="sxs-lookup"><span data-stu-id="a17c1-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a17c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a17c1-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="a17c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a17c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a17c1-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-108">Die Anzahl der zu aktualisierenden Striche.</span><span class="sxs-lookup"><span data-stu-id="a17c1-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="a17c1-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-110">Ein Array, das die Strich Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="a17c1-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a17c1-111">*ulstrokepacketdescriptioncount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-112">Die Anzahl der Eigenschaften in jedem Paket.</span><span class="sxs-lookup"><span data-stu-id="a17c1-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="a17c1-113">*pstrokepacketdescriptionguids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-114">Ein Array, das die Paket Eigenschaften Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="a17c1-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="a17c1-115">*pulpacketdatacountperstroke* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-116">Ein Array, das die Anzahl der Pakete in jedem Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="a17c1-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="a17c1-117">*plstrokepacketdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a17c1-118">Ein Array, das die Paketdaten für die Striche enthält.</span><span class="sxs-lookup"><span data-stu-id="a17c1-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a17c1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a17c1-119">Return value</span></span>

<span data-ttu-id="a17c1-120">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a17c1-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a17c1-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a17c1-121">Remarks</span></span>

<span data-ttu-id="a17c1-122">der *plstrokepacketdata* -Parameter enthält Paketdaten für alle Striche.</span><span class="sxs-lookup"><span data-stu-id="a17c1-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="a17c1-123">Der *pstrokepacketdescriptionguids* -Parameter enthält die Global Unique Identifier (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt in jedem Strich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a17c1-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="a17c1-124">Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a17c1-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="a17c1-125">Nur Striche mit denselben Paketbeschreibungen können in einem einzelnen **iinkanalyzer:: UpdateStrokesData-Methode** aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a17c1-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="a17c1-126">Mit dieser Methode wird der geänderte Bereich der Ink Analyzer nicht aktualisiert (Weitere Informationen finden Sie unter [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="a17c1-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="a17c1-127">Wenn ein angegebener Strich nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist, ignoriert diese Methode den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a17c1-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="a17c1-128">Wenn keiner der angegebenen Striche einen Strich identifiziert, der dem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet ist, gibt diese Methode zurück, ohne **iinkanalyzer** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a17c1-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="a17c1-129">Diese Methode gibt einen Fehlercode zurück, wenn *plstrokeids* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="a17c1-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a17c1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a17c1-130">Requirements</span></span>



| <span data-ttu-id="a17c1-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a17c1-131">Requirement</span></span> | <span data-ttu-id="a17c1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a17c1-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a17c1-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a17c1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a17c1-134">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a17c1-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a17c1-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a17c1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a17c1-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a17c1-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a17c1-137">Header</span><span class="sxs-lookup"><span data-stu-id="a17c1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a17c1-138"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a17c1-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a17c1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a17c1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a17c1-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17c1-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a17c1-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a17c1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17c1-142">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a17c1-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a17c1-143">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="a17c1-144">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a17c1-145">**Iinkanalyzer:: addstrokedecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a17c1-146">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a17c1-147">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a17c1-148">**Iinkanalyzer:: addstrokestocustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a17c1-149">**Iinkanalyzer:: ClearStrokeData-Methode**</span><span class="sxs-lookup"><span data-stu-id="a17c1-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="a17c1-150">**\_Ianalysil Vents:: updatestrokescache**</span><span class="sxs-lookup"><span data-stu-id="a17c1-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="a17c1-151">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a17c1-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




