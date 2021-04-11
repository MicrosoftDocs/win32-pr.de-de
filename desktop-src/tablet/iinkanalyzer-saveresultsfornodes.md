---
description: Speichert Analyseergebnisse für eine bestimmte Kontext Knoten Sammlung, die mit einem iinkanalyzer verknüpft ist.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Iinkanalyzer:: saveresultsfornodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129444"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="4058a-103">Iinkanalyzer:: saveresultsfornodes-Methode</span><span class="sxs-lookup"><span data-stu-id="4058a-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="4058a-104">Speichert Analyseergebnisse für eine bestimmte Kontext Knoten Sammlung, die mit einem [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4058a-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4058a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4058a-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="4058a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4058a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4058a-107">*pcontextnodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4058a-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4058a-108">Die [**icontextnode**](icontextnode.md) -Auflistung, für die Analyseergebnisse gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4058a-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="4058a-109">*pulserializeddatasize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4058a-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4058a-110">Die Anzahl der Bytes in *ppbserializeddata*.</span><span class="sxs-lookup"><span data-stu-id="4058a-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="4058a-111">*ppbserializeddata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4058a-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4058a-112">Zeiger auf die serialisierten Analysedaten.</span><span class="sxs-lookup"><span data-stu-id="4058a-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4058a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4058a-113">Return value</span></span>

<span data-ttu-id="4058a-114">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4058a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4058a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4058a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4058a-116">Um einen Speicherplatz zu vermeiden, müssen Sie für ppbserializeddata " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, \*  Wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="4058a-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="4058a-117">Diese Methode speichert die aktuellen Analyseergebnisse für die [**icontextnode**](icontextnode.md) -Objekte in *pcontextnodes* und alle deren Vorgänger-und Nachfolger Kontext Knoten.</span><span class="sxs-lookup"><span data-stu-id="4058a-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="4058a-118">Diese Methode speichert keine Strich Daten.</span><span class="sxs-lookup"><span data-stu-id="4058a-118">This method does not save any stroke data.</span></span> <span data-ttu-id="4058a-119">Es liegt in der Verantwortung der Anwendung, alle Analyseergebnisse und die zugehörigen hubdaten zu synchronisieren, falls Sie weiterhin vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4058a-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="4058a-120">Wenn das zu speichernde [**icontextnode**](icontextnode.md) -Objekt nur teilweise aufgefüllt ist, gibt diese Methode einen Fehlercode zurück (siehe [**icontextnode:: getpartiallygefüllte**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="4058a-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4058a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4058a-121">Requirements</span></span>



| <span data-ttu-id="4058a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4058a-122">Requirement</span></span> | <span data-ttu-id="4058a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4058a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4058a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4058a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4058a-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4058a-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4058a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4058a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4058a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4058a-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4058a-128">Header</span><span class="sxs-lookup"><span data-stu-id="4058a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4058a-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4058a-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4058a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4058a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4058a-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4058a-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4058a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4058a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4058a-133">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="4058a-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4058a-134">**Iinkanalyzer:: loadresults-Methode**</span><span class="sxs-lookup"><span data-stu-id="4058a-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="4058a-135">**Iinkanalyzer:: SaveResults-Methode**</span><span class="sxs-lookup"><span data-stu-id="4058a-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="4058a-136">**Iinkanalyzer:: saveresultsforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="4058a-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4058a-137">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="4058a-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4058a-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4058a-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

