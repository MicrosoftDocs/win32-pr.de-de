---
description: Ruft den Stamm-icontextnode der Kontext Struktur des iinkanalyzer-Objekts ab.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Iinkanalyzer:: GetRootNode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348418"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="59894-103">Iinkanalyzer:: GetRootNode-Methode</span><span class="sxs-lookup"><span data-stu-id="59894-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="59894-104">Ruft den Stamm- [**icontextnode**](icontextnode.md) der Kontext Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="59894-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="59894-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59894-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="59894-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59894-107">*pprootnode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59894-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59894-108">Der Stamm- [**icontextnode**](icontextnode.md) der Kontext Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="59894-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59894-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59894-109">Return value</span></span>

<span data-ttu-id="59894-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="59894-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59894-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59894-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="59894-112">Um einen Speicherfehler zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *pprootnode* , wenn Sie den Stamm Knoten nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="59894-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="59894-113">[**Iinkanalyzer**](iinkanalyzer.md) verwaltet eine Struktur von [**icontextnode**](icontextnode.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="59894-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="59894-114">Diese Objekte enthalten sowohl Eingaben für die Analyse als auch die Ergebnisse der Analyse.</span><span class="sxs-lookup"><span data-stu-id="59894-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="59894-115">Wenn dem **iinkanalyzer** anfänglich Striche hinzugefügt werden, weist **iinkanalyzer** diese einem **icontextnode** vom Typ unclassiatedink zu (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="59894-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="59894-116">Nachdem die Striche analysiert wurden, werden Sie von **iinkanalyzer** den entsprechenden **icontextnode** -Objekten in der Struktur zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="59894-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="59894-117">Weitere Informationen zur Verwendung von " **iinkanalyzer** " zur Analyse von frei Hand Eingaben finden Sie unter [Übersicht über die Ink-Analyse](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="59894-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="59894-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59894-118">Examples</span></span>

<span data-ttu-id="59894-119">Das folgende Beispiel zeigt eine Methode, die die [**icontextnode**](icontextnode.md) -Ergebnis Struktur der Ink Analyzer durchläuft.</span><span class="sxs-lookup"><span data-stu-id="59894-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="59894-120">Wenn der iinkanlyzer zurzeit keine frei Hand Analyse ausführt, führt die-Methode Folgendes aus.</span><span class="sxs-lookup"><span data-stu-id="59894-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="59894-121">Ruft die Top-Erkennungs Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="59894-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="59894-122">Ruft den Stamm Knoten der Ink Analyzer ab.</span><span class="sxs-lookup"><span data-stu-id="59894-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="59894-123">Ruft die Hilfsmethode `ExploreContextNode` auf, um den Stamm Knoten und seine untergeordneten Knoten zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="59894-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="59894-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59894-124">Requirements</span></span>



| <span data-ttu-id="59894-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59894-125">Requirement</span></span> | <span data-ttu-id="59894-126">Wert</span><span class="sxs-lookup"><span data-stu-id="59894-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59894-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59894-127">Minimum supported client</span></span><br/> | <span data-ttu-id="59894-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59894-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="59894-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59894-129">Minimum supported server</span></span><br/> | <span data-ttu-id="59894-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59894-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="59894-131">Header</span><span class="sxs-lookup"><span data-stu-id="59894-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="59894-132"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="59894-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="59894-133">DLL</span><span class="sxs-lookup"><span data-stu-id="59894-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59894-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59894-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="59894-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59894-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59894-136">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="59894-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="59894-137">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="59894-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="59894-138">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="59894-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="59894-139">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="59894-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

