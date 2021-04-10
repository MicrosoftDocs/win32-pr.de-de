---
description: Speichert alle Analyseergebnisse für einen iinkanalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Iinkanalyzer:: SaveResults-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343679"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="5a140-103">Iinkanalyzer:: SaveResults-Methode</span><span class="sxs-lookup"><span data-stu-id="5a140-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="5a140-104">Speichert alle Analyseergebnisse für einen [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="5a140-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a140-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a140-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="5a140-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a140-107">*pulserializeddatasize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a140-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a140-108">Die Anzahl der Bytes in *ppbserializeddata*.</span><span class="sxs-lookup"><span data-stu-id="5a140-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="5a140-109">*ppbserializeddata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a140-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a140-110">Ein Array, das die gespeicherten Analyseergebnisse enthält.</span><span class="sxs-lookup"><span data-stu-id="5a140-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a140-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a140-111">Return value</span></span>

<span data-ttu-id="5a140-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5a140-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a140-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a140-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5a140-114">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbserializeddata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="5a140-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="5a140-115">Diese Methode speichert alle aktuellen Analyseergebnisse, einschließlich aktueller Analyse Hinweis und benutzerdefinierter Erkennungs Knoten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="5a140-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="5a140-116">Diese Methode speichert keine Strich Daten.</span><span class="sxs-lookup"><span data-stu-id="5a140-116">This method does not save any stroke data.</span></span> <span data-ttu-id="5a140-117">Es liegt in der Verantwortung der Anwendung, Analyseergebnisse und entsprechende Striche zu synchronisieren, wenn Sie Daten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5a140-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="5a140-118">Diese Methode gibt einen Fehlercode zurück, wenn ein [**icontextnode**](icontextnode.md) -Objekt zum Speichern teilweise aufgefüllt wird (siehe [**icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="5a140-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a140-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a140-119">Requirements</span></span>



| <span data-ttu-id="5a140-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a140-120">Requirement</span></span> | <span data-ttu-id="5a140-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5a140-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a140-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a140-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5a140-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a140-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5a140-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a140-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5a140-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5a140-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5a140-126">Header</span><span class="sxs-lookup"><span data-stu-id="5a140-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a140-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5a140-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5a140-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5a140-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a140-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a140-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5a140-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a140-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a140-131">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="5a140-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5a140-132">**Iinkanalyzer:: loadresults-Methode**</span><span class="sxs-lookup"><span data-stu-id="5a140-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="5a140-133">**Iinkanalyzer:: saveresultsfornodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="5a140-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="5a140-134">**Iinkanalyzer:: saveresultsforstrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="5a140-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="5a140-135">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="5a140-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5a140-136">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="5a140-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

