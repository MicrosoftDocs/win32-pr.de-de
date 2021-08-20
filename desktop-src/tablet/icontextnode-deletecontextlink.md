---
description: Löscht ein IContextLink-Objekt aus der Linkauflistung des IContextNode-Objekts.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: IContextNode::D eleteContextLink-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 39a36ed8a74accdc7da3eed4c98a96d9ee6abbaa4f52b5c71c367250321d28b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044841"
---
# <a name="icontextnodedeletecontextlink-method"></a>IContextNode::D eleteContextLink-Methode

Löscht ein [**IContextLink-Objekt**](icontextlink.md) aus der Linkauflistung des [**IContextNode-Objekts.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContextLinkToDelete* \[ In\]
</dt> <dd>

Das zu löschende [**IContextLink-Objekt.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Ein Kontextlink verfügt über einen Quellknoten und einen Zielknoten (siehe [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) und [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)). Diese Methode entfernt den [**IContextLink**](icontextlink.md) aus der Auflistung der Kontextlinks des Quell- und Zielknotens (siehe [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




