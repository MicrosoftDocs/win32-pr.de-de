---
description: Stellt eine Warnung oder einen Fehler dar, die während eines frei Hand Analyse Vorgangs auftritt.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Ianalysiswarning-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129516"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="fa2d7-103">Ianalysiswarning-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fa2d7-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="fa2d7-104">Stellt eine Warnung oder einen Fehler dar, die während eines frei Hand Analyse Vorgangs auftritt.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="fa2d7-105">Member</span><span class="sxs-lookup"><span data-stu-id="fa2d7-105">Members</span></span>

<span data-ttu-id="fa2d7-106">Die **ianalysiswarning** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fa2d7-107">**Ianalysiswarning** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa2d7-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="fa2d7-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa2d7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa2d7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="fa2d7-109">Methods</span></span>

<span data-ttu-id="fa2d7-110">Die **ianalysiswarning** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="fa2d7-111">Methode</span><span class="sxs-lookup"><span data-stu-id="fa2d7-111">Method</span></span>                                                            | <span data-ttu-id="fa2d7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa2d7-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa2d7-113">**Getbackgrounderror**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="fa2d7-114">Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="fa2d7-115">**GetHint**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="fa2d7-116">Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="fa2d7-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="fa2d7-118">Ruft die Bezeichner aller relevanten Kontext Knoten ab, die dieser Warnung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="fa2d7-119">**Getwarningcode**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="fa2d7-120">Ruft den Typ der Warnung ab, die mithilfe der [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Enumeration aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa2d7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa2d7-121">Remarks</span></span>

<span data-ttu-id="fa2d7-122">Die Typen von Warnungen, die auftreten können, werden durch die [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Enumeration beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="fa2d7-123">Warnungen treten häufig auf, wenn Sie versuchen, eine Funktion zu verwenden, die von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) nicht unterstützt wird, die von [**iinkanalyzer**](iinkanalyzer.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="fa2d7-124">Einige Warnungen weisen darauf hin, dass der [**iinkanalyzer**](iinkanalyzer.md) den Analyse Vorgang nicht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="fa2d7-125">Weitere Informationen finden Sie unter [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="fa2d7-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="fa2d7-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa2d7-126">Examples</span></span>

<span data-ttu-id="fa2d7-127">Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="fa2d7-128">Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="fa2d7-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="fa2d7-129">Wenn der Analyse Vorgang Warnungen generiert, durchläuft der Handler die Auflistung von **ianalysiswarning** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="fa2d7-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fa2d7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa2d7-130">Requirements</span></span>



| <span data-ttu-id="fa2d7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa2d7-131">Requirement</span></span> | <span data-ttu-id="fa2d7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fa2d7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2d7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa2d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2d7-134">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa2d7-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa2d7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa2d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2d7-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fa2d7-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fa2d7-137">Header</span><span class="sxs-lookup"><span data-stu-id="fa2d7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2d7-138"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa2d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2d7-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2d7-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fa2d7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa2d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2d7-142">**Ianalysiswarning**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="fa2d7-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="fa2d7-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="fa2d7-144">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="fa2d7-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

