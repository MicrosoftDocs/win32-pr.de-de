---
description: Ruft die Ink-Blattknoten ab, die die angegebenen Striche enthalten.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: IInkAnalyzer::FindInkLeafNodesForStrokes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a7424f62008e15feb538df7a6a27745dda17bf6ace4612218608f8e509e75e59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967279"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>IInkAnalyzer::FindInkLeafNodesForStrokes-Methode

Ruft die Ink-Blattknoten ab, die die angegebenen Striche enthalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der übergebenen Strichbezeichner.

</dd> <dt>

*plStrokeIds* \[ In\]
</dt> <dd>

Ein Array der Strichbezeichner.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Die Auflistung von [**IContextNode-Objekten,**](icontextnode.md) die alle Ink-Blattknoten enthalten, die die Striche mit Bezeichnern im *plStrokeIds-Array* enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodesFound* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Blattknoten enthalten keine untergeordneten Knoten. Ink-Knoten enthalten Strichdaten. Beispiele für Freihandblattknoten sind InkWord-, InkDrawing- [**undInkBullet-IContextNode-Objekte.**](icontextnode.md) Weitere Informationen finden Sie unter [Kontextknotentypen.](context-node-types.md)

Wenn keine Knoten die angegebenen Striche enthalten, wird eine leere [**IContextNodes-Auflistung**](icontextnodes.md) zurückgegeben. Wenn *ulStrokeIdsCount* gleich 0 (null) ist, wird eine leere **IContextNodes-Auflistung** zurückgegeben.

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

[**IInkAnalyzer::FindInkLeafNodes-Methode**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindLeafNodes-Methode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindNode-Methode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeInSubTree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

