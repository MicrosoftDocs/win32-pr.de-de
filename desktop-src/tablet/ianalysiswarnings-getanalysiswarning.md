---
description: Ruft das ianalysiswarning-Objekt am angegebenen Index ab.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'Ianalysiswarning:: getanalysiswarning-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041769"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="4f13c-103">Ianalysiswarning:: getanalysiswarning-Methode</span><span class="sxs-lookup"><span data-stu-id="4f13c-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="4f13c-104">Ruft das [**ianalysiswarning**](ianalysiswarning.md) -Objekt am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="4f13c-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f13c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f13c-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="4f13c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f13c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f13c-107">*ulindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f13c-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13c-108">Der null basierte Index des abzurufenden [**ianalysiswarning**](ianalysiswarning.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4f13c-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="4f13c-109">*ppwarning* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4f13c-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f13c-110">Ein Zeiger auf das [**ianalysiswarning**](ianalysiswarning.md) -Objekt am angegebenen Index.</span><span class="sxs-lookup"><span data-stu-id="4f13c-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f13c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f13c-111">Return value</span></span>

<span data-ttu-id="4f13c-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f13c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f13c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f13c-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4f13c-114">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) bei \* *ppwarning* , wenn Sie die Warnung nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="4f13c-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4f13c-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f13c-115">Examples</span></span>

<span data-ttu-id="4f13c-116">Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4f13c-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="4f13c-117">Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="4f13c-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="4f13c-118">Wenn der Analyse Vorgang Warnungen generiert, durchläuft der Handler die Auflistung von [**ianalysiswarning**](ianalysiswarning.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="4f13c-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4f13c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f13c-119">Requirements</span></span>



| <span data-ttu-id="4f13c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f13c-120">Requirement</span></span> | <span data-ttu-id="4f13c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4f13c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f13c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f13c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4f13c-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f13c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f13c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f13c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4f13c-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4f13c-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f13c-126">Header</span><span class="sxs-lookup"><span data-stu-id="4f13c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f13c-127"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f13c-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f13c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4f13c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f13c-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f13c-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f13c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f13c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f13c-131">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="4f13c-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="4f13c-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4f13c-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

