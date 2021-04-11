---
description: Ruft das icontextnode-Objekt für eine angegebene Globally Unique Identifier (GUID) ab.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Iinkanalyzer:: FindNode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041761"
---
# <a name="iinkanalyzerfindnode-method"></a>Iinkanalyzer:: FindNode-Methode

Ruft das [**icontextnode**](icontextnode.md) -Objekt für eine angegebene Globally Unique Identifier (GUID) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ in\]
</dt> <dd>

Der Bezeichner für das [**icontextnode**](icontextnode.md) -Objekt.

</dd> <dt>

*ppcontextnode found* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt mit dem *pId* -Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnounfound* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Wenn kein solches [**icontextnode**](icontextnode.md) -Objekt als Nachfolger des Stamm Knotens [**iinkanalyzer**](iinkanalyzer.md) vorhanden ist, wird **null** zurückgegeben.

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

 

