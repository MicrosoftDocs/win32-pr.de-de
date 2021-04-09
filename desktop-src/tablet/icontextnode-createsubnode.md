---
description: Erstellt ein neues untergeordnetes icontextnode-Objekt.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Icontextnode:: kreatesubnode-Methode (iacom. h)'
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
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862720"
---
# <a name="icontextnodecreatesubnode-method"></a>Icontextnode:: kreatesubnode-Methode

Erstellt ein neues untergeordnetes [**icontextnode**](icontextnode.md) -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnodetype* \[ in\]
</dt> <dd>

Eine **GUID** , die den Typ des zu erstellenden [**icontextnode**](icontextnode.md) darstellt.

</dd> <dt>

*ppcontextnode created* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den neuen [**icontextnode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppcontextnodecreated* , wenn Sie den Kontext Knoten nicht mehr verwenden müssen.

 

Der neue [**icontextnode**](icontextnode.md) wird der Auflistung von untergeordneten Knoten dieses Kontext Knotens hinzugefügt (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)). Wenn vorhandene untergeordnete Knoten vorhanden sind, wird der neu erstellte **icontextnode** als letzter untergeordneter Knoten hinzugefügt.

Eine Liste der Kontext Knoten Typen finden Sie unter [Kontext Knoten Typen](context-node-types.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode::D eletesubnode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

