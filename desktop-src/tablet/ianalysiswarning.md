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
# <a name="ianalysiswarning-interface"></a>Ianalysiswarning-Schnittstelle

Stellt eine Warnung oder einen Fehler dar, die während eines frei Hand Analyse Vorgangs auftritt.

## <a name="members"></a>Member

Die **ianalysiswarning** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ianalysiswarning** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ianalysiswarning** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Getbackgrounderror**](ianalysiswarning-getbackgrounderror.md) | Ruft den Fehlercode für den Vorgang der Hintergrund Handschrift Analyse ab, wenn ein Fehler aufgetreten ist.<br/>                                    |
| [**GetHint**](ianalysiswarning-gethint.md)                       | Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.<br/>                                                                        |
| [**GetNodeIds**](ianalysiswarning-getnodeids.md)                 | Ruft die Bezeichner aller relevanten Kontext Knoten ab, die dieser Warnung zugeordnet sind.<br/>                              |
| [**Getwarningcode**](ianalysiswarning-getwarningcode.md)         | Ruft den Typ der Warnung ab, die mithilfe der [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Enumeration aufgetreten ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Typen von Warnungen, die auftreten können, werden durch die [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Enumeration beschrieben. Warnungen treten häufig auf, wenn Sie versuchen, eine Funktion zu verwenden, die von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) nicht unterstützt wird, die von [**iinkanalyzer**](iinkanalyzer.md) verwendet wird.

Einige Warnungen weisen darauf hin, dass der [**iinkanalyzer**](iinkanalyzer.md) den Analyse Vorgang nicht abgeschlossen hat. Weitere Informationen finden Sie unter [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis. Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md). Wenn der Analyse Vorgang Warnungen generiert, durchläuft der Handler die Auflistung von **ianalysiswarning** -Objekten.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysiswarning**](ianalysiswarnings.md)
</dt> <dt>

[**AnalysisWarningCode**](analysiswarningcode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

