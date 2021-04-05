---
description: Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in iinkanalyzer ab.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Iinkanalyzer:: GetRecognizedString-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751808"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="7897b-103">Iinkanalyzer:: GetRecognizedString-Methode</span><span class="sxs-lookup"><span data-stu-id="7897b-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="7897b-104">Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in [**iinkanalyzer**](iinkanalyzer.md)ab.</span><span class="sxs-lookup"><span data-stu-id="7897b-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7897b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7897b-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="7897b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7897b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7897b-107">*pbstrauerkenzedstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7897b-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7897b-108">Die beste Ergebnis Zeichenfolge des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7897b-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7897b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7897b-109">Return value</span></span>

<span data-ttu-id="7897b-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7897b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7897b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7897b-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7897b-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**sysfrestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für *pbstrauerkenzedstring* , wenn Sie die Zeichenfolge nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="7897b-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="7897b-113">Diese Methode gibt den gleichen Wert wie die Eigenschaften Daten des Stamm Knotens für die erkannte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7897b-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="7897b-114">(Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md), [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)und [Kontext Knoten Eigenschaften](context-node-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="7897b-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="7897b-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7897b-115">Examples</span></span>

<span data-ttu-id="7897b-116">Das folgende Beispiel zeigt eine Methode, die die [**icontextnode**](icontextnode.md) -Ergebnis Struktur der Ink Analyzer durchläuft.</span><span class="sxs-lookup"><span data-stu-id="7897b-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="7897b-117">Wenn der iinkanlyzer zurzeit keine frei Hand Analyse ausführt, führt die-Methode Folgendes aus.</span><span class="sxs-lookup"><span data-stu-id="7897b-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="7897b-118">Ruft die Top-Erkennungs Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="7897b-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="7897b-119">Ruft den Stamm Knoten der Ink Analyzer ab.</span><span class="sxs-lookup"><span data-stu-id="7897b-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="7897b-120">Ruft die Hilfsmethode `ExploreContextNode` auf, um den Stamm Knoten und seine untergeordneten Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="7897b-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7897b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7897b-121">Requirements</span></span>



| <span data-ttu-id="7897b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7897b-122">Requirement</span></span> | <span data-ttu-id="7897b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7897b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7897b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7897b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7897b-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7897b-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7897b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7897b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7897b-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7897b-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7897b-128">Header</span><span class="sxs-lookup"><span data-stu-id="7897b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7897b-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7897b-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7897b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7897b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7897b-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7897b-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7897b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7897b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7897b-133">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="7897b-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7897b-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="7897b-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

