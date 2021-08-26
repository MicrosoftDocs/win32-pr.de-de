---
description: Ruft alle IContextNode-Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen IContextNode-Objekts sind.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d6ab8e66e75af4e31a1efacd082f79f68d5f63c546c56d59bf4ca0fedc201929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939930"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode

Ruft alle [**IContextNode-Objekte**](icontextnode.md) ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen **IContextNode-Objekts** sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCriteria* \[ In\]
</dt> <dd>

Ein [**IMatchesCriteriaCallBack-Objekt,**](imatchescriteriacallback.md) das verwendet wird, um auszuwerten, ob ein [**IContextNode-Objekt**](icontextnode.md) die angegebenen Kriterien erfüllt oder nicht.

</dd> <dt>

*pContextNodeToSearchFrom* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) dessen Nachfolger durchsucht werden.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Ein Zeiger auf [**IContextNodes,**](icontextnodes.md) der alle Knoten enthält, die die angegebenen Kriterien erfüllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppContextNodesFound* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Wenn der [**IInkAnalyzer**](iinkanalyzer.md) den Knoten *pContextNodeToSearchFrom* nicht enthält, gibt diese Methode einen Fehlercode zurück.

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

[**IInkAnalyzer::FindNodesOfTypeInSubTree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

