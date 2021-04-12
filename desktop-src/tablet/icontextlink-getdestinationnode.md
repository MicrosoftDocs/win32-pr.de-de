---
description: Ruft das icontextnode-Objekt ab, das das Ziel für diesen icontextlink ist.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'Icontextlink:: getdestinationnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343728"
---
# <a name="icontextlinkgetdestinationnode-method"></a>Icontextlink:: getdestinationnode-Methode

Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das das Ziel für diesen [**icontextlink**](icontextlink.md)ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdstcontextnodeid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextnode**](icontextnode.md) -Objekt, das das Ziel für diesen [**icontextlink**](icontextlink.md)ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppdstcontextnodeid* , wenn Sie den Zielknoten nicht mehr verwenden müssen.

 

Wenn das [**icontextlink**](icontextlink.md) -Objekt zwischen einem Knoten mit Schreibvorgang und einem Knoten mit Zeichnung verknüpft ist, ist der Zielknoten in der Regel der Knoten, der Schreibvorgänge enthält.

Wenn das [**icontextlink**](icontextlink.md) -Objekt den Linktyp engeschlossen aufweist (siehe [**icontextlink:: getcontextlinkdirection**](icontextlink-getcontextlinkdirection.md)), ist der Zielknoten das [**icontextnode**](icontextnode.md) -Objekt, das eingeschlossen ist.

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

[**Icontextlink:: getsourcenode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

