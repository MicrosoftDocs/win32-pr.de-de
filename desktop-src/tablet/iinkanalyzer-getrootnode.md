---
description: Ruft den Stamm-icontextnode der Kontext Struktur des iinkanalyzer-Objekts ab.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Iinkanalyzer:: GetRootNode-Methode (iacom. h)'
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
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348418"
---
# <a name="iinkanalyzergetrootnode-method"></a>Iinkanalyzer:: GetRootNode-Methode

Ruft den Stamm- [**icontextnode**](icontextnode.md) der Kontext Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprootnode* \[ vorgenommen\]
</dt> <dd>

Der Stamm- [**icontextnode**](icontextnode.md) der Kontext Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherfehler zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *pprootnode* , wenn Sie den Stamm Knoten nicht mehr verwenden müssen.

 

[**Iinkanalyzer**](iinkanalyzer.md) verwaltet eine Struktur von [**icontextnode**](icontextnode.md) -Objekten. Diese Objekte enthalten sowohl Eingaben für die Analyse als auch die Ergebnisse der Analyse. Wenn dem **iinkanalyzer** anfänglich Striche hinzugefügt werden, weist **iinkanalyzer** diese einem **icontextnode** vom Typ unclassiatedink zu (siehe [**icontextnode:: GetType**](icontextnode-gettype.md) und [Kontext Knoten Typen](context-node-types.md)). Nachdem die Striche analysiert wurden, werden Sie von **iinkanalyzer** den entsprechenden **icontextnode** -Objekten in der Struktur zugewiesen. Weitere Informationen zur Verwendung von " **iinkanalyzer** " zur Analyse von frei Hand Eingaben finden Sie unter [Übersicht über die Ink-Analyse](ink-analysis-overview.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Methode, die die [**icontextnode**](icontextnode.md) -Ergebnis Struktur der Ink Analyzer durchläuft. Wenn der iinkanlyzer zurzeit keine frei Hand Analyse ausführt, führt die-Methode Folgendes aus.

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

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

