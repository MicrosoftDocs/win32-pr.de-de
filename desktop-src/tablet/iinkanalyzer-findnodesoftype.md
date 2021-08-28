---
description: Ruft alle IContextNode-Objekte des angegebenen Typs ab.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: IInkAnalyzer::FindNodesOfType-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ab35825c47ddbbdeda3affc0ab0585dce111233990db28ae65a0636f7145ce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939958"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a>IInkAnalyzer::FindNodesOfType-Methode

Ruft alle [**IContextNode-Objekte**](icontextnode.md) des angegebenen Typs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNodeType* \[ In\]
</dt> <dd>

Die **GUID,** die den Knotentyp angibt.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Ein Zeiger auf die [**IContextNodes,**](icontextnodes.md) die alle Knoten vom Typ *pNodeType enthalten.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodesFound* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Die *pNodeType-Eigenschaft* muss eine GUID aus den [Konstanten für Kontextknotentypen](context-node-types.md) enthalten.

Wenn [**IInkAnalyzer keinen**](iinkanalyzer.md) solchen [**IContextNode**](icontextnode.md)enthält, wird eine leere [**IContextNodes-Auflistung**](icontextnodes.md) zurückgegeben.

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

[**IInkAnalyzer::FindInkLeafNodesForStrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindLeafNodes-Methode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**IInkAnalyzer::FindNode-Methode**](iinkanalyzer-findnode.md)
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

 

