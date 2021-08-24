---
description: Ruft den IContextNode-Stamm der Kontextstruktur des IInkAnalyzer-Objekts ab.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: IInkAnalyzer::GetRootNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5ff2181eacd3df1d2815448a0c2d7cafce4d521fa0abbc7b26492d9c078982dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713420"
---
# <a name="iinkanalyzergetrootnode-method"></a>IInkAnalyzer::GetRootNode-Methode

Ruft den [**IContextNode-Stamm**](icontextnode.md) der Kontextstruktur des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppRootNode* \[ out\]
</dt> <dd>

Der [**Stamm-IContextNode**](icontextnode.md) der Kontextstruktur des [**IInkAnalyzer-Objekts.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppRootNode* auf, wenn Sie den Stammknoten nicht mehr verwenden müssen.

 

[**IInkAnalyzer**](iinkanalyzer.md) verwaltet eine Struktur von [**IContextNode-Objekten.**](icontextnode.md) Diese Objekte enthalten sowohl Eingaben für die Analyse als auch die Ergebnisse der Analyse. Wenn **IInkAnalyzer** anfänglich Striche hinzugefügt werden, weist **IInkAnalyzer** sie einem **IContextNode** vom Typ UnclassifiedInk zu (siehe [**IContextNode::GetType**](icontextnode-gettype.md) und [Kontextknotentypen](context-node-types.md)). Nachdem die Striche analysiert wurden, weist **IInkAnalyzer** sie den entsprechenden **IContextNode-Objekten** in der Struktur zu. Weitere Informationen zur Verwendung von **IInkAnalyzer** zum Analysieren von Freihanddaten finden Sie unter Übersicht über die [Freihandanalyse.](ink-analysis-overview.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

