---
description: Ruft das icontextnode-Objekt ab, das die Quelle für diesen icontextlink ist.
ms.assetid: 2f55ae9c-9f63-4d49-9bf0-9e169b819e79
title: 'Icontextlink:: getsourcenode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetSourceNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eddab21740bf30c67e247cec89723bc47cd9dca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214672"
---
# <a name="icontextlinkgetsourcenode-method"></a>Icontextlink:: getsourcenode-Methode

Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das die Quelle für diesen [**icontextlink**](icontextlink.md)ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSourceNode(
  [out] IContextNode **ppSrcContextNodeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsrccontextnodeid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das die Quelle für diesen [**icontextlink**](icontextlink.md)ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppsrccontextnodeid* , wenn Sie den Quellknoten nicht mehr verwenden müssen.

 

Wenn das [**icontextlink**](icontextlink.md) -Objekt zwischen einem Knoten mit Schreibvorgang und einem Knoten mit Zeichnung verknüpft ist, ist der Quellknoten in der Regel der Knoten, der die Zeichnung enthält.

Wenn das [**icontextlink**](icontextlink.md) -Objekt den Linktyp engeschlossen aufweist (siehe [**icontextlink:: getcontextlinkdirection**](icontextlink-getcontextlinkdirection.md)), ist der Quellknoten der Knoten, der den Zielknoten einschließt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextlink**](icontextlink.md)
</dt> <dt>

[**Icontextlink:: getdestinationnode**](icontextlink-getdestinationnode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

