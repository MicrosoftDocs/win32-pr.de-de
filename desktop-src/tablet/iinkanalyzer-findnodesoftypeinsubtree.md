---
description: Ruft alle IContextNode-Objekte des angegebenen Typs ab, die Nachfolger des angegebenen IContextNode-Objekts sind.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: IInkAnalyzer::FindNodesOfTypeInSubTree-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 16e1516a8da5b4d09b80606bad5cf5f9444d82545394543c46b06a05425befa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939946"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>IInkAnalyzer::FindNodesOfTypeInSubTree-Methode

Ruft alle [**IContextNode-Objekte**](icontextnode.md) des angegebenen Typs ab, die Nachfolger des angegebenen **IContextNode-Objekts** sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNodeType* \[ In\]
</dt> <dd>

Die **GUID,** die den Knotentyp angibt.

</dd> <dt>

*pContextNodeToSearchFrom* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) dessen Nachfolger durchsucht werden.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Die [**IContextNodes-Auflistung,**](icontextnodes.md) die alle Knoten vom Typ *pNodeType* enthält, die Nachfolger von *pContextNodeToSearchFrom* sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodesFound* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn der [**IInkAnalyzer**](iinkanalyzer.md) den Knoten *pContextNodeToSearchFrom* nicht enthält, gibt diese Methode einen Fehlercode zurück.

Die *pNodeType-Eigenschaft* muss einen GUID (Globally Unique Identifier) aus den [Konstanten für Kontextknotentypen](context-node-types.md) enthalten.

Wenn [**IInkAnalyzer**](iinkanalyzer.md) keinen solchen [**IContextNode**](icontextnode.md)enthält, wird eine leere [**IContextNodes-Auflistung**](icontextnodes.md) zurückgegeben.

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

[**IInkAnalyzer::FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

