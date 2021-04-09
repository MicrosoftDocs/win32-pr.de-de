---
description: Ruft die frei Hand Blattknoten ab, die die angegebenen Striche enthalten.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Iinkanalyzer:: findinkleafnodesforstrokes-Methode (iacom. h)'
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
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862692"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Iinkanalyzer:: findinkleafnodesforstrokes-Methode

Ruft die frei Hand Blattknoten ab, die die angegebenen Striche enthalten.

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

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der über gebenen Strich Bezeichner.

</dd> <dt>

*plstrokeids* \[ in\]
</dt> <dd>

Ein Array der Strich Bezeichner.

</dd> <dt>

*ppcontextnodesfound* \[ vorgenommen\]
</dt> <dd>

Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, die alle frei Hand Blattknoten enthalten, die die Striche mit bezeichern im *plstrokeids* -Array enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Blattknoten enthalten keine untergeordneten Knoten. Frei Hand Knoten enthalten Strich Daten. Beispiele für frei Hand Blattknoten sind InkWord-, InkDrawing-und andinkbullet- [**icontextnode**](icontextnode.md) -Objekte. Weitere Informationen finden Sie unter [Kontext Knoten Typen](context-node-types.md).

Wenn keine Knoten die angegebenen Striche enthalten, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben. Wenn *ulstrokeidscount* gleich 0 (null) ist, wird eine leere **icontextnodes** -Auflistung zurückgegeben.

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

[**Iinkanalyzer:: FindInkLeafNodes-Methode**](iinkanalyzer-findinkleafnodes.md)
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

 

