---
description: Ruft alle icontextnode-Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen icontextnode-Objekts sind.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode (iacom. h)'
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
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751825"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode

Ruft alle [**icontextnode**](icontextnode.md) -Objekte ab, die den angegebenen Kriterien entsprechen und Nachfolger des angegebenen **icontextnode** -Objekts sind.

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

*pcriteria* \[ in\]
</dt> <dd>

Ein [**imatchescriteria**](imatchescriteriacallback.md) -Objekt, das verwendet wird, um zu überprüfen, ob ein [**icontextnode**](icontextnode.md) -Objekt die angegebenen Kriterien erfüllt oder nicht.

</dd> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, dessen Nachfolgern durchsucht werden.

</dd> <dt>

*ppcontextnodesfound* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die [**icontextnodes**](icontextnodes.md) , die alle Knoten enthält, die die angegebenen Kriterien erfüllen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodesfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Wenn [**iinkanalyzer**](iinkanalyzer.md) den *pcontextnodedesearchfrom* -Knoten nicht enthält, gibt diese Methode einen Fehlercode zurück.

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

[**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

