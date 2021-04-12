---
description: Ruft eine boolesche Zusammenfassung der Ergebnisse des Analyse Vorgangs ab.
ms.assetid: 9bc690f4-fb5f-449e-bde0-bd2277c4573b
title: 'Ianalysisstatus:: iserfolgreiches-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.IsSuccessful
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: daf7ec801773d855f0ed85a795bc492ef673a74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343738"
---
# <a name="ianalysisstatusissuccessful-method"></a><span data-ttu-id="45131-103">Ianalysisstatus:: iserfolgreiches-Methode</span><span class="sxs-lookup"><span data-stu-id="45131-103">IAnalysisStatus::IsSuccessful method</span></span>

<span data-ttu-id="45131-104">Ruft eine boolesche Zusammenfassung der Ergebnisse des Analyse Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="45131-104">Retrieves a Boolean summary of the results of the analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="45131-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45131-105">Syntax</span></span>


```C++
HRESULT IsSuccessful(
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="45131-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45131-107">*pferfolgreich* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="45131-107">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45131-108">**Variant \_ TRUE** , wenn der Analyse Vorgang ohne Warnungen abgeschlossen wurde, oder **Variant \_ false** , wenn mindestens eine Warnung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="45131-108">**VARIANT\_TRUE** if the analysis operation completed without any warnings, or **VARIANT\_FALSE** if at least one warning occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45131-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45131-109">Return value</span></span>

<span data-ttu-id="45131-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="45131-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="45131-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45131-111">Examples</span></span>

<span data-ttu-id="45131-112">Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="45131-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="45131-113">Der Handler überprüft **ianalysisstatus:: iserfolg**.</span><span class="sxs-lookup"><span data-stu-id="45131-113">The handler checks **IAnalysisStatus::IsSuccessful**.</span></span> <span data-ttu-id="45131-114">Wenn der Analyse Vorgang Warnungen generiert, durchläuft der Handler die Auflistung von [**ianalysiswarning**](ianalysiswarning.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="45131-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="45131-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45131-115">Requirements</span></span>



| <span data-ttu-id="45131-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45131-116">Requirement</span></span> | <span data-ttu-id="45131-117">Wert</span><span class="sxs-lookup"><span data-stu-id="45131-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45131-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45131-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45131-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45131-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45131-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45131-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45131-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="45131-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="45131-122">Header</span><span class="sxs-lookup"><span data-stu-id="45131-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45131-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="45131-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="45131-124">DLL</span><span class="sxs-lookup"><span data-stu-id="45131-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45131-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45131-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="45131-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45131-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45131-127">**Ianalysisstatus**</span><span class="sxs-lookup"><span data-stu-id="45131-127">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="45131-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="45131-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




