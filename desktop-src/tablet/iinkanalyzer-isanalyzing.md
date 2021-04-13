---
description: Ruft einen Wert ab, der angibt, ob iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Iinkanalyzer:: isanalytics-Methode (iacom. h)'
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
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526489"
---
# <a name="iinkanalyzerisanalyzing-method"></a>Iinkanalyzer:: isanalysierungsmethode

Ruft einen Wert ab, der angibt, ob [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbanalyalisierung* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist **Variant \_ true** , wenn [**iinkanalyzer**](iinkanalyzer.md) eine synchrone oder asynchrone Analyse ausführt.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die die [**icontextnode**](icontextnode.md) -Ergebnis Struktur der Ink Analyzer durchläuft. Wenn die frei Hand Analyse zurzeit keine frei Hand Analyse durchführt, führt die-Methode Folgendes aus.

-   Ruft die Top-Erkennungs Zeichenfolge ab.
-   Ruft den Stamm Knoten der Ink Analyzer ab.
-   Ruft die Hilfsmethode `ExploreContextNode` auf, um den Stamm Knoten und seine untergeordneten Knoten zu untersuchen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




