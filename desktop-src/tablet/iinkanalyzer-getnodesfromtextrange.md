---
description: Ruft eine Auflistung von IContextNode-Objekten ab, die für den angegebenen Textbereich für die angegebenen Kontextknoten relevant sind.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: IInkAnalyzer::GetNodesFromTextRange-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df9eb6e1e748088abaa4780aedfded4e26977018d70dd79f518159185594a90b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057820"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a>IInkAnalyzer::GetNodesFromTextRange-Methode

Ruft eine Auflistung von [**IContextNode-Objekten**](icontextnode.md) ab, die für den angegebenen Textbereich für die angegebenen Kontextknoten relevant sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plStart* \[ in, out\]
</dt> <dd>

Ein Verweis auf den Anfang des Textbereichs im *pNodesToSearch-Teil* der erkannten Zeichenfolge.

</dd> <dt>

*plLength* \[ in, out\]
</dt> <dd>

Ein Verweis auf die Länge des Textbereichs im *pNodesToSearch-Teil* der erkannten Zeichenfolge.

</dd> <dt>

*ppContextNodes* \[ out\]
</dt> <dd>

Ein Zeiger auf die [**IContextNode-Objekte,**](icontextnode.md) die für den angegebenen Textbereich für die angegebenen Kontextknoten relevant sind.

</dd> <dt>

*pNodesToSearch* \[ In\]
</dt> <dd>

Die [**IContextNode-Objekte,**](icontextnode.md) auf die die Suche beschränkt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Der angegebene Textbereich sollte relativ zum *pNodesToSearch-Teil* der erkannten Zeichenfolge von [**IInkAnalyzer**](iinkanalyzer.md)und nicht zur erkannten Zeichenfolge des gesamten **IInkAnalyzer-Werts** sein.

Diese Methode ändert die Werte der *PlStart-* und *plLength-Parameter,* indem der Textbereich auf die nächsten Wortgrenzen erweitert wird.

Wenn die erkannte Zeichenfolge beispielsweise "Ich bin spät" lautet und Sie diese Methode mithilfe der Parameterwerte 6 für *plStart* und 1 für *plLength* aufrufen, was dem Buchstaben "a" in "late" entspricht, gibt diese Methode eine Auflistung zurück, die einen einzelnen [**IContextNode,**](icontextnode.md)das InkWord oder TextWord enthält, das dem Wort "late" entspricht. In diesem Beispiel ändert diese Methode auch den Wert von *plStart* in 5 und den Wert von *plLength* auf 4, was dem Wort "late" entspricht.

> [!Note]  
> Der *plStart-Parameter* ist relativ zur erkannten Zeichenfolge des *pNodesToSearch-Parameters.*

 

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
</dt> </dl>

 

 




