---
description: Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in iinkanalyzer ab.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Iinkanalyzer:: GetRecognizedString-Methode (iacom. h)'
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
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751808"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a>Iinkanalyzer:: GetRecognizedString-Methode

Ruft die Zeichenfolge mit dem besten Ergebnis des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in [**iinkanalyzer**](iinkanalyzer.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrauerkenzedstring* \[ vorgenommen\]
</dt> <dd>

Die beste Ergebnis Zeichenfolge des Erkennungs Vorgangs für die gesamte Kontext Knoten Struktur in [**iinkanalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**sysfrestring**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für *pbstrauerkenzedstring* , wenn Sie die Zeichenfolge nicht mehr verwenden müssen.

 

Diese Methode gibt den gleichen Wert wie die Eigenschaften Daten des Stamm Knotens für die erkannte Zeichenfolge zurück. (Weitere Informationen finden Sie unter [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md), [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)und [Kontext Knoten Eigenschaften](context-node-properties.md).)

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

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

