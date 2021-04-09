---
description: Ruft alle icontextnode-Objekte des angegebenen Typs ab.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Iinkanalyzer:: findnodesoft ype-Methode (iacom. h)'
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
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862691"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a>Iinkanalyzer:: findnodesoft ype-Methode

Ruft alle [**icontextnode**](icontextnode.md) -Objekte des angegebenen Typs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnodetype* \[ in\]
</dt> <dd>

Der **GUID** , der den Knotentyp angibt.

</dd> <dt>

*ppcontextnodesfound* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) , die alle Knoten des Typs " *pnodetype*" enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Die *pnodetype* -Eigenschaft muss eine GUID aus den [Kontext Knoten Typen](context-node-types.md) Konstanten enthalten.

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

 

