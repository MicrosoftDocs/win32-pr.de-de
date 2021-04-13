---
description: Ruft einen Wert ab, der angibt, ob iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Iinkanalyzer:: isanalytics-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526489"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="943dc-103">Iinkanalyzer:: isanalysierungsmethode</span><span class="sxs-lookup"><span data-stu-id="943dc-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="943dc-104">Ruft einen Wert ab, der angibt, ob [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="943dc-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="943dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="943dc-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="943dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="943dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="943dc-107">*pbanalyalisierung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="943dc-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="943dc-108">**Variant \_ TRUE** , wenn [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="943dc-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="943dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="943dc-109">Return value</span></span>

<span data-ttu-id="943dc-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="943dc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="943dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="943dc-111">Remarks</span></span>

<span data-ttu-id="943dc-112">Diese Eigenschaft ist **Variant \_ true** , wenn [**iinkanalyzer**](iinkanalyzer.md) eine synchrone oder asynchrone Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="943dc-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="943dc-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="943dc-113">Examples</span></span>

<span data-ttu-id="943dc-114">Das folgende Beispiel zeigt eine Methode, die die [**icontextnode**](icontextnode.md) -Ergebnis Struktur der Ink Analyzer durchläuft.</span><span class="sxs-lookup"><span data-stu-id="943dc-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="943dc-115">Wenn die frei Hand Analyse zurzeit keine frei Hand Analyse durchführt, führt die-Methode Folgendes aus.</span><span class="sxs-lookup"><span data-stu-id="943dc-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="943dc-116">Ruft die Top-Erkennungs Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="943dc-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="943dc-117">Ruft den Stamm Knoten der Ink Analyzer ab.</span><span class="sxs-lookup"><span data-stu-id="943dc-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="943dc-118">Ruft die Hilfsmethode `ExploreContextNode` auf, um den Stamm Knoten und seine untergeordneten Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="943dc-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="943dc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="943dc-119">Requirements</span></span>



| <span data-ttu-id="943dc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="943dc-120">Requirement</span></span> | <span data-ttu-id="943dc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="943dc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943dc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="943dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="943dc-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="943dc-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="943dc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="943dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="943dc-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="943dc-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="943dc-126">Header</span><span class="sxs-lookup"><span data-stu-id="943dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="943dc-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="943dc-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="943dc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="943dc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943dc-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="943dc-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="943dc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="943dc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943dc-131">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="943dc-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="943dc-132">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="943dc-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="943dc-133">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="943dc-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="943dc-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="943dc-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




