---
description: Enthält eine Auflistung von -Objekten, die die IAnalysisWarning-Schnittstelle implementieren und das Ergebnis eines Ink-Analyse-Vorgangs sind.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: IAnalysisWarnings-Schnittstelle (IACom.h)
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
ms.openlocfilehash: 6a14e11400c6af564ccab86fc08746b8185fefba98aa472544981534b902f8ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057950"
---
# <a name="ianalysiswarnings-interface"></a>IAnalysisWarnings-Schnittstelle

Enthält eine Auflistung von -Objekten, die die [**IAnalysisWarning-Schnittstelle**](ianalysiswarning.md) implementieren und das Ergebnis eines Ink-Analyse-Vorgangs sind.

## <a name="members"></a>Member

Die **IAnalysisWarnings-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisWarnings verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAnalysisWarnings-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisWarning**](ianalysiswarnings-getanalysiswarning.md) | Ruft das [**IAnalysisWarning-Objekt**](ianalysiswarning.md) am angegebenen Index ab.<br/>                                       |
| [**GetCount**](ianalysiswarnings-getcount.md)                     | Ruft die Anzahl der [**IAnalysisWarning-Objekte**](ianalysiswarning.md) ab, die in der **IAnalysisWarnings-Auflistung enthalten** sind.<br/> |



 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Gliederung eines Ereignishandlers für das [**\_ IAnalysisEvents::Results-Ereignis.**](-ianalysisevents-results.md) Der Handler überprüft [**IAnalysisStatus::IsSuccessful.**](ianalysisstatus-issuccessful.md) Wenn der Analysevorgang Warnungen generiert hat, durchfing der Handler die Auflistung von [**IAnalysisWarning-Objekten.**](ianalysiswarning.md)


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

