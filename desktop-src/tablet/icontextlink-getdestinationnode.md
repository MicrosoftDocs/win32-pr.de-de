---
description: Ruft das IContextNode-Objekt ab, das das Ziel für diesen IContextLink ist.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: IContextLink::GetDestinationNode-Methode (IACom.h)
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
ms.openlocfilehash: 1a11d9021d4299a1823fee57ed9a80237b4896459b0396a8ba4b140bd377bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967454"
---
# <a name="icontextlinkgetdestinationnode-method"></a>IContextLink::GetDestinationNode-Methode

Ruft das [**IContextNode-Objekt**](icontextnode.md) ab, das das Ziel für diesen [**IContextLink ist.**](icontextlink.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDstContextNodeId* \[ out\]
</dt> <dd>

Ein Zeiger auf das [**IContextNode-Objekt,**](icontextnode.md) das das Ziel für diesen [**IContextLink ist.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppDstContextNodeId* auf, wenn Sie den Zielknoten nicht mehr verwenden müssen.

 

Wenn das [**IContextLink-Objekt**](icontextlink.md) zwischen einem Knoten mit Schreib- und einem Knoten mit Zeichnung verknüpft ist, ist der Zielknoten in der Regel der Knoten, der schreibt.

Wenn das [**IContextLink-Objekt**](icontextlink.md) über den Linktyp "Encloses" verfügt (siehe [**IContextLink::GetContextLinkDirection),**](icontextlink-getcontextlinkdirection.md)ist der Zielknoten das [**eingeschlossene IContextNode-Objekt.**](icontextnode.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**Contextlinkdirection**](contextlinkdirection.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

