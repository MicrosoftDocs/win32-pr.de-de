---
description: Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungsvorgangs für die gesamte Kontextknotenstruktur im IInkAnalyzer ab.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: IInkAnalyzer::GetRecognizedString-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3defa68f68e0c2e81bdb093005db1e173442b9686ca4c98a4966c755b2fb52dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092248"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>IInkAnalyzer::GetRecognizedString-Methode

Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungsvorgangs für die gesamte Kontextknotenstruktur im [**IInkAnalyzer**](iinkanalyzer.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Die zeichenfolge mit dem besten Ergebnis des Erkennungsvorgangs für die gesamte Kontextknotenstruktur in [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für *pbstrRecognizedString* auf, wenn Sie die Zeichenfolge nicht mehr verwenden müssen.

 

Diese Methode gibt den gleichen Wert wie die Eigenschaftsdaten des Stammknotens für die erkannte Zeichenfolge zurück. (Siehe [**IInkAnalyzer::GetRootNode-Methode,**](iinkanalyzer-getrootnode.md) [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)und [Kontextknoteneigenschaften](context-node-properties.md).)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die die [**IContextNode-Ergebnisstruktur**](icontextnode.md) des Ink-Analysetools durchläuft. Wenn der IInkAnlyzer derzeit keine Freihandanalyse durchführt, führt die Methode folgende Schritte aus.

-   Ruft die oberste Erkennungszeichenfolge ab.
-   Ruft den Stammknoten des Ink-Analysetools ab.
-   Ruft die Hilfsmethode `ExploreContextNode` auf, um den Stammknoten und seine untergeordneten Knoten zu untersuchen.


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

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

