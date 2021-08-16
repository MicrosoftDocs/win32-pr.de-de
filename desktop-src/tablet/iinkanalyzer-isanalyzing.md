---
description: Ruft einen Wert ab, der angibt, ob der IInkAnalyzer eine Ink-Analyse vorgibt.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: IInkAnalyzer::IsAnalyzing-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1dc0a10bfcafb5972413eb1d1d0880a63db69498c38481cc0cbf6bb58e5f69f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092050"
---
# <a name="iinkanalyzerisanalyzing-method"></a>IInkAnalyzer::IsAnalyzing-Methode

Ruft einen Wert ab, der angibt, ob [**der IInkAnalyzer**](iinkanalyzer.md) eine Ink-Analyse vorgibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbAnalyzing* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn [**der IInkAnalyzer**](iinkanalyzer.md) eine Ink-Analyse durchfing; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist **VARIANT \_ TRUE,** wenn [**der IInkAnalyzer**](iinkanalyzer.md) synchrone oder asynchrone Analysen vorsteuert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die die [**IContextNode-Ergebnisstruktur**](icontextnode.md) des Ink Analyzers durchfingt. Wenn die Ink-Analyse derzeit keine Ink-Analyse durchfing, führt die -Methode Folgendes aus.

-   Ruft die oberste Erkennungszeichenfolge ab.
-   Ruft den Stammknoten des Ink Analyzers ab.
-   Ruft die Hilfsmethode auf, `ExploreContextNode` um den Stammknoten und seine untergeordneten Knoten zu untersuchen.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




