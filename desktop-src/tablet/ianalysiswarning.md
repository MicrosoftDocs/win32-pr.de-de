---
description: Stellt eine Warnung oder einen Fehler dar, die während eines Ink-Analyse-Vorgangs auftritt.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: IAnalysisWarning-Schnittstelle (IACom.h)
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
ms.openlocfilehash: 27e00533894560a84e73f8eb5682d1b70789ab5f2b21be5d6fe3682c543be6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940380"
---
# <a name="ianalysiswarning-interface"></a>IAnalysisWarning-Schnittstelle

Stellt eine Warnung oder einen Fehler dar, die während eines Ink-Analyse-Vorgangs auftritt.

## <a name="members"></a>Member

Die **IAnalysisWarning-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisWarning** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAnalysisWarning-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBackgroundError**](ianalysiswarning-getbackgrounderror.md) | Ruft den Fehlercode für den Hintergrund-Ink-Analysevorgang ab, wenn ein Fehler aufgetreten ist.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Ruft den Analysehinweis ab, der diese Warnung verursacht hat.<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Ruft die Bezeichner aller relevanten Kontextknoten ab, die dieser Warnung zugeordnet sind.<br/>                              |
| [**GetWarningCode**](ianalysiswarning-getwarningcode.md)         | Ruft den Typ der Warnung ab, die mithilfe der [**AnalysisWarningCode-Enumeration aufgetreten**](/windows/desktop/tablet/analysiswarningcode) ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Typen von Warnungen, die auftreten können, werden von der [**AnalysisWarningCode-Enumeration**](/windows/desktop/tablet/analysiswarningcode) beschrieben. Häufig werden Warnungen angezeigt, wenn Sie versuchen, eine Funktion zu verwenden, die nicht vom [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) unterstützt wird, den [**IInkAnalyzer**](iinkanalyzer.md) verwendet.

Einige Warnungen deuten darauf hin, dass [**IInkAnalyzer**](iinkanalyzer.md) den Analysevorgang nicht abgeschlossen hat. Weitere Informationen finden Sie unter [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Gliederung eines Ereignishandlers für das [**\_ IAnalysisEvents::Results-Ereignis.**](-ianalysisevents-results.md) Der Handler überprüft [**IAnalysisStatus::IsSuccessful.**](ianalysisstatus-issuccessful.md) Wenn der Analysevorgang Warnungen generiert, durch iteriert der Handler die Auflistung von **IAnalysisWarning-Objekten.**


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

[**IAnalysisWarnings**](ianalysiswarnings.md)
</dt> <dt>

[**Analysiswarningcode**](analysiswarningcode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

