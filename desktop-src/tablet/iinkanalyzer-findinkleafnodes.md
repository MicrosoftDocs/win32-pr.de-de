---
description: Ruft alle frei Hand Blattknoten ab.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Iinkanalyzer:: FindInkLeafNodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862696"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a>Iinkanalyzer:: FindInkLeafNodes-Methode

Ruft alle frei Hand Blattknoten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppcontextnodesfound* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) -Auflistung, die alle frei Hand Blattknoten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Blattknoten enthalten keine untergeordneten Knoten. Frei Hand Knoten enthalten Strich Daten. Beispiele für frei Hand Blattknoten sind InkWord-, InkDrawing-und InkBullet- [**icontextnode**](icontextnode.md) -Objekte. Weitere Informationen finden Sie unter [Kontext Knoten Typen](context-node-types.md).

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

[**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: findleafnodes-Methode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Iinkanalyzer:: FindNode-Methode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ype-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

