---
description: Speichert Analyseergebnisse für die angegebenen Striche, die einem iinkanalyzer zugeordnet sind.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Iinkanalyzer:: saveresultsforstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343678"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="78307-103">Iinkanalyzer:: saveresultsforstrokes-Methode</span><span class="sxs-lookup"><span data-stu-id="78307-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="78307-104">Speichert Analyseergebnisse für die angegebenen Striche, die einem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="78307-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78307-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78307-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="78307-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78307-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78307-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78307-108">Die Anzahl der Stroke-IDs in **plstrokeids**.</span><span class="sxs-lookup"><span data-stu-id="78307-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="78307-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78307-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78307-110">Das Array von Strich bezeichlern.</span><span class="sxs-lookup"><span data-stu-id="78307-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="78307-111">*pulserializeddatasize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="78307-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78307-112">Die Anzahl der Bytes in *ppbserializeddata*.</span><span class="sxs-lookup"><span data-stu-id="78307-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="78307-113">*ppbserializeddata* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="78307-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="78307-114">Zeiger auf die serialisierten Analysedaten.</span><span class="sxs-lookup"><span data-stu-id="78307-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78307-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78307-115">Return value</span></span>

<span data-ttu-id="78307-116">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="78307-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78307-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78307-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="78307-118">Um einen Speicherplatz zu vermeiden, müssen Sie für ppbserializeddata " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, \*  Wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="78307-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="78307-119">Diese Methode speichert die aktuellen Analyseergebnisse für die angegebenen Striche.</span><span class="sxs-lookup"><span data-stu-id="78307-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="78307-120">Diese Methode speichert die frei Hand Blatt- [**icontextnode**](icontextnode.md) -Objekte, die die Striche und alle übergeordneten Knoten dieser Kontext Knoten enthalten.</span><span class="sxs-lookup"><span data-stu-id="78307-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="78307-121">Diese Methode speichert keine Stroke-Daten oder Analyse Hinweis Knoten.</span><span class="sxs-lookup"><span data-stu-id="78307-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="78307-122">Es liegt in der Verantwortung der Anwendung, alle Analyseergebnisse und die zugehörigen hubdaten zu synchronisieren, falls Sie weiterhin vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="78307-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="78307-123">Diese Methode gibt einen Fehlercode zurück, wenn ein [**icontextnode**](icontextnode.md) -Objekt zum Speichern teilweise aufgefüllt wird (siehe [**icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="78307-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="78307-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78307-124">Requirements</span></span>



| <span data-ttu-id="78307-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78307-125">Requirement</span></span> | <span data-ttu-id="78307-126">Wert</span><span class="sxs-lookup"><span data-stu-id="78307-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78307-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78307-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78307-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78307-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78307-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78307-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78307-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="78307-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="78307-131">Header</span><span class="sxs-lookup"><span data-stu-id="78307-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78307-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78307-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78307-133">DLL</span><span class="sxs-lookup"><span data-stu-id="78307-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78307-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78307-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="78307-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78307-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78307-136">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="78307-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="78307-137">**Iinkanalyzer:: loadresults-Methode**</span><span class="sxs-lookup"><span data-stu-id="78307-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="78307-138">**Iinkanalyzer:: SaveResults-Methode**</span><span class="sxs-lookup"><span data-stu-id="78307-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="78307-139">**Iinkanalyzer:: saveresultsfornodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="78307-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="78307-140">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="78307-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="78307-141">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="78307-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

