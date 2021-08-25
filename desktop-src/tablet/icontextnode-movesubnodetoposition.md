---
description: Ordnet ein angegebenes untergeordnetes IContextNode-Objekt dem angegebenen Index neu an.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: IContextNode::MoveSubNodeToPosition-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d48876be10a2c45daca62b3175a358d31ed128ddd3bcb045c052e2d51308c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773820"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>IContextNode::MoveSubNodeToPosition-Methode

Ordnet ein angegebenes untergeordnetes [**IContextNode-Objekt**](icontextnode.md) dem angegebenen Index neu an.

## <a name="syntax"></a>Syntax


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSubnodeToMove* \[ In\]
</dt> <dd>

Das [**zu verschiebende IContextNode-Objekt.**](icontextnode.md)

</dd> <dt>

*ulNewIndex* \[ In\]
</dt> <dd>

Der Index für die neue Position des Unternodes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Gibt **E \_ INVALIDARG** zurück, *wenn pSubnodeToMove* kein untergeordneter Knoten dieses [**IContextNode ist.**](icontextnode.md)

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

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




