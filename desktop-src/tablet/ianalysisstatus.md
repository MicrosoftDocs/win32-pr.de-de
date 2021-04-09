---
description: Stellt den Status des frei Hand Analyse Vorgangs dar, indem beschrieben wird, ob die Analyse erfolgreich abgeschlossen wurde und ob Warnungen aufgetreten sind.
ms.assetid: 57910a1d-3472-4689-ba0d-a220145e77c4
title: Ianalysisstatus-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e14f7fabea8090f5471513eca524f6fcdb939b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129520"
---
# <a name="ianalysisstatus-interface"></a>Ianalysisstatus-Schnittstelle

Stellt den Status des frei Hand Analyse Vorgangs dar, indem beschrieben wird, ob die Analyse erfolgreich abgeschlossen wurde und ob Warnungen aufgetreten sind.

## <a name="members"></a>Member

Die **ianalysisstatus** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ianalysisstatus** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ianalysisstatus** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                                                                                                                                    |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getappliedchangesregion**](ianalysisstatus-getappliedchangesregion.md) | Ruft den Bereich des Dokuments ab, der den Änderungen entspricht, die in der Kontext Knoten Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts als Ergebnis einer frei Hand Analyse vorgenommen wurden.<br/> |
| [**GetWarnings**](ianalysisstatus-getwarnings.md)                         | Ruft eine [**ianalysiswarning**](ianalysiswarnings.md) -Auflistung ab, die alle Fehler und Warnungen beschreibt, die vom Analyse Vorgang generiert werden.<br/>                                  |
| [**IsSuccessful**](ianalysisstatus-issuccessful.md)                       | Ruft eine boolesche Zusammenfassung der Ergebnisse des Analyse Vorgangs ab.<br/>                                                                                                               |



 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Gliederung eines Ereignis Handlers für das [**\_ ianalysil Vents:: results**](-ianalysisevents-results.md) -Ereignis. Der Handler überprüft [**ianalysisstatus:: iserfolg**](ianalysisstatus-issuccessful.md). Wenn der Analyse Vorgang Warnungen generiert, durchläuft der Handler die Auflistung von [**ianalysiswarning**](ianalysiswarning.md) -Objekten.


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

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

