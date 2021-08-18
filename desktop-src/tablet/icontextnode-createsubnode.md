---
description: Erstellt ein neues untergeordnetes IContextNode-Objekt.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: IContextNode::CreateSubNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7b4bc39431d6b4608586e60bdeffb7cd6c79bf95f944e436c16a683e24e634d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092311"
---
# <a name="icontextnodecreatesubnode-method"></a>IContextNode::CreateSubNode-Methode

Erstellt ein neues untergeordnetes [**IContextNode-Objekt.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNodeType* \[ In\]
</dt> <dd>

Eine **GUID,** die den Typ des zu [**erstellenden IContextNode**](icontextnode.md) darstellt.

</dd> <dt>

*ppContextNodeCreated* \[ out\]
</dt> <dd>

Ein Zeiger auf den neuen [**IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppContextNodeCreated* auf, wenn Sie den Kontextknoten nicht mehr verwenden müssen.

 

Der neue [**IContextNode**](icontextnode.md) wird der Auflistung untergeordneter Knoten dieses Kontextknotens hinzugefügt (siehe [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Wenn untergeordnete Knoten vorhanden sind, wird der neu erstellte **IContextNode** als letzter untergeordneter Knoten hinzugefügt.

Eine Liste der Kontextknotentypen finden Sie unter [Kontextknotentypen.](context-node-types.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

