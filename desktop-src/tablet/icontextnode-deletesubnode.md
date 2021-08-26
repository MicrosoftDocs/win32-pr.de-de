---
description: Entfernt einen untergeordneten IContextNode.
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: IContextNode::D eleteSubNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0ebad42f02ccfad0db2d119832f3495819ac18ce321d72ede3aa8d7545b999be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057880"
---
# <a name="icontextnodedeletesubnode-method"></a>IContextNode::D eleteSubNode-Methode

Entfernt einen untergeordneten [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContextNodeToDelete* \[ In\]
</dt> <dd>

Der [**zu entfernende IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

E \_ INVALIDARG wird zurückgegeben, wenn der *pContextNodeToDelete-Parameter* kein untergeordnetes Element dieses [**IContextNode-Objekts**](icontextnode.md) ist.

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

 

 




