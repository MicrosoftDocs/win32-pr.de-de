---
description: Gibt die Bezeichner aller relevanten Kontext Knoten zurück, die dieser Warnung zugeordnet sind.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Ianalysiswarning:: GetNodeIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526540"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="094cc-103">Ianalysiswarning:: GetNodeIds-Methode</span><span class="sxs-lookup"><span data-stu-id="094cc-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="094cc-104">Gibt die Bezeichner aller relevanten Kontext Knoten zurück, die dieser Warnung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="094cc-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="094cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="094cc-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="094cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="094cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="094cc-107">*pulCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="094cc-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="094cc-108">Die Anzahl der global eindeutigen Bezeichner (GUIDs) in *ppnodeids*.</span><span class="sxs-lookup"><span data-stu-id="094cc-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="094cc-109">*ppnodeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="094cc-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="094cc-110">Ein Zeiger auf ein Array von GUIDs, das die dieser Analyse Warnung zugeordneten Kontext Knoten identifiziert, oder **null** , wenn der Warnung keine Kontext Knoten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="094cc-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="094cc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="094cc-111">Return value</span></span>

<span data-ttu-id="094cc-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="094cc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="094cc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="094cc-113">Remarks</span></span>

<span data-ttu-id="094cc-114">Wenn *ppnodeids* als **null**-Werte übermittelt wird, gibt die **GetNodeIds** -Methode **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="094cc-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="094cc-115">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppnodeids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="094cc-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="094cc-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="094cc-116">Examples</span></span>

<span data-ttu-id="094cc-117">Im folgenden Beispiel wird gezeigt, wie Sie die [**icontextnode**](icontextnode.md) -Objekte, die sich in [**ianalysiswarning**](ianalysiswarning.md)befinden, `warning` sowie die Anzahl der **icontextnode** -Objekte erhalten.</span><span class="sxs-lookup"><span data-stu-id="094cc-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="094cc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="094cc-118">Requirements</span></span>



| <span data-ttu-id="094cc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="094cc-119">Requirement</span></span> | <span data-ttu-id="094cc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="094cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094cc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="094cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="094cc-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="094cc-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="094cc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="094cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="094cc-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="094cc-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="094cc-125">Header</span><span class="sxs-lookup"><span data-stu-id="094cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="094cc-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="094cc-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="094cc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="094cc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="094cc-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="094cc-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="094cc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="094cc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094cc-130">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="094cc-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="094cc-131">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="094cc-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="094cc-132">**Iinkanalyzer:: FindNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="094cc-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="094cc-133">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="094cc-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

