---
description: Enthält eine Auflistung von-Objekten, die die ianalysiswarning-Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Ianalysiswarning-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357354"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="774b0-103">Ianalysiswarning-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="774b0-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="774b0-104">Enthält eine Auflistung von-Objekten, die die [**ianalysiswarning**](ianalysiswarning.md) -Schnittstelle implementieren und die das Ergebnis eines frei Hand Analyse Vorgangs sind.</span><span class="sxs-lookup"><span data-stu-id="774b0-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="774b0-105">Member</span><span class="sxs-lookup"><span data-stu-id="774b0-105">Members</span></span>

<span data-ttu-id="774b0-106">Die **ianalysiswarning** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="774b0-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="774b0-107">**Ianalysiswarning** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="774b0-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="774b0-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="774b0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="774b0-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="774b0-109">Methods</span></span>

<span data-ttu-id="774b0-110">Die **ianalysiswarning** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="774b0-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="774b0-111">Methode</span><span class="sxs-lookup"><span data-stu-id="774b0-111">Method</span></span>                                                             | <span data-ttu-id="774b0-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="774b0-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="774b0-113">**Getanalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="774b0-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="774b0-114">Ruft das [**ianalysiswarning**](ianalysiswarning.md) -Objekt am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="774b0-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="774b0-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="774b0-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="774b0-116">Ruft die Anzahl der [**ianalysiswarning**](ianalysiswarning.md) -Objekte ab, die in der **ianalysiswarning** -Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="774b0-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="774b0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="774b0-117">Examples</span></span>

<span data-ttu-id="774b0-118">Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="774b0-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="774b0-119">Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="774b0-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="774b0-120">Wenn der Analyse Vorgang Warnungen generiert hat, durchläuft der Handler die Auflistung von [**ianalysiswarning**](ianalysiswarning.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="774b0-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="774b0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="774b0-121">Requirements</span></span>



| <span data-ttu-id="774b0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="774b0-122">Requirement</span></span> | <span data-ttu-id="774b0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="774b0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774b0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="774b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="774b0-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="774b0-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="774b0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="774b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="774b0-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="774b0-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="774b0-128">Header</span><span class="sxs-lookup"><span data-stu-id="774b0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="774b0-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="774b0-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="774b0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="774b0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="774b0-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="774b0-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="774b0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="774b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774b0-133">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="774b0-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="774b0-134">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="774b0-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="774b0-135">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="774b0-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

