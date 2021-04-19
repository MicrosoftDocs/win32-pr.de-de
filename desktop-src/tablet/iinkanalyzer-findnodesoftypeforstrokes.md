---
description: Ruft alle icontextnode-Objekte des angegebenen Typs ab, die die angegebenen Striche enthalten.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346957"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode

Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab, die die angegebenen Striche enthalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnodetype* \[ in\]
</dt> <dd>

Der Globally Unique Identifier (GUID), der den Knotentyp angibt.

</dd> <dt>

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

Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, die alle Knoten vom Typ " *pnodetype* " enthalten, die die Striche mit bezeichern im *plstrokeids* -Array enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Die *pnodetype* -Eigenschaft muss eine GUID aus den [Kontext Knoten Typen](context-node-types.md) Konstanten enthalten.

Wenn der angegebene Knotentyp kein Blattknoten ist, aber einer der untergeordneten Knoten auf einen Strich in der Striche-Auflistung verweist, wird dieser Knoten der zurückgegebenen Auflistung hinzugefügt.

Wenn [**iinkanalyzer**](iinkanalyzer.md) keinen derartigen [**icontextnode**](icontextnode.md)enthält, wird eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zurückgegeben.

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

[**Iinkanalyzer:: findinkleafnodesforstrokes-Methode**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: findleafnodes-Methode**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Iinkanalyzer:: FindNode-Methode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ype-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

