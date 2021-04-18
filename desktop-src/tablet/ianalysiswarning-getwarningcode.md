---
description: Gibt den Typ der Warnung zurück, die mithilfe der AnalysisWarningCode-Enumeration aufgetreten ist.
ms.assetid: ec67a5ac-a7a2-4805-b9b5-915ea956d228
title: 'Ianalysiswarning:: getwarningcode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetWarningCode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e129b410de9e8ca9e3944b6a371fe0cac673fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345081"
---
# <a name="ianalysiswarninggetwarningcode-method"></a><span data-ttu-id="69e71-103">Ianalysiswarning:: getwarningcode-Methode</span><span class="sxs-lookup"><span data-stu-id="69e71-103">IAnalysisWarning::GetWarningCode method</span></span>

<span data-ttu-id="69e71-104">Gibt den Typ der Warnung zurück, die mithilfe der [**AnalysisWarningCode**](analysiswarningcode.md) -Enumeration aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="69e71-104">Returns the type of warning that occurred by using the [**AnalysisWarningCode**](analysiswarningcode.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e71-105">Syntax</span></span>


```C++
HRESULT GetWarningCode(
  [out] AnalysisWarningCode *pWarningCode
);
```



## <a name="parameters"></a><span data-ttu-id="69e71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69e71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e71-107">*pwarningcode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="69e71-107">*pWarningCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69e71-108">Der Typ der Warnung, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="69e71-108">The type of warning that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e71-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69e71-109">Return value</span></span>

<span data-ttu-id="69e71-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="69e71-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="69e71-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69e71-111">Examples</span></span>

<span data-ttu-id="69e71-112">Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69e71-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="69e71-113">Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="69e71-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="69e71-114">Wenn der Analyse Vorgang Warnungen generiert hat, durchläuft der Handler die Auflistung von [**ianalysiswarning**](ianalysiswarning.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="69e71-114">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="69e71-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69e71-115">Requirements</span></span>



| <span data-ttu-id="69e71-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69e71-116">Requirement</span></span> | <span data-ttu-id="69e71-117">Wert</span><span class="sxs-lookup"><span data-stu-id="69e71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e71-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69e71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69e71-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69e71-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69e71-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69e71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69e71-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="69e71-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69e71-122">Header</span><span class="sxs-lookup"><span data-stu-id="69e71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e71-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="69e71-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69e71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="69e71-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69e71-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e71-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69e71-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69e71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e71-127">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="69e71-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="69e71-128">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="69e71-128">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="69e71-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="69e71-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

