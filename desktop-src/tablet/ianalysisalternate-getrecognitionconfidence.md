---
description: Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der iinkanalyzer in der Genauigkeit von ianalysisalternate hat.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Ianalysisalternate:: getrecognitionconfidence-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751881"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="8604c-103">Ianalysisalternate:: getrecognitionconfidence-Methode</span><span class="sxs-lookup"><span data-stu-id="8604c-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="8604c-104">Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit von [**ianalysisalternate**](ianalysisalternate.md)hat.</span><span class="sxs-lookup"><span data-stu-id="8604c-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8604c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8604c-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="8604c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8604c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8604c-107">*pconfidence* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8604c-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8604c-108">Ein Zeiger auf eine [**InkRecognitionConfidence-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) , die die Vertrauens Ebene angibt, die von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) in der Genauigkeit der Erkennungs Alternativen liegt.</span><span class="sxs-lookup"><span data-stu-id="8604c-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8604c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8604c-109">Return value</span></span>

<span data-ttu-id="8604c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8604c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8604c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8604c-111">Requirements</span></span>



| <span data-ttu-id="8604c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8604c-112">Requirement</span></span> | <span data-ttu-id="8604c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8604c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8604c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8604c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8604c-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8604c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8604c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8604c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8604c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8604c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8604c-118">Header</span><span class="sxs-lookup"><span data-stu-id="8604c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8604c-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8604c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8604c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8604c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8604c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8604c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8604c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8604c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8604c-123">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="8604c-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="8604c-124">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="8604c-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8604c-125">**Iinkanalysiserkenzer**</span><span class="sxs-lookup"><span data-stu-id="8604c-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8604c-126">**Erkentionconfidence**</span><span class="sxs-lookup"><span data-stu-id="8604c-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="8604c-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="8604c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




