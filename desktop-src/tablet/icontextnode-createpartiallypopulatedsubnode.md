---
description: Erstellt ein untergeordnetes IContextNode-Objekt, das nur Informationen zu Typ, Bezeichner und Speicherort enthält.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: IContextNode::CreatePartiallyPopulatedSubNode-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7233c6e0303f0634c71a67fde13f237feb2b2f6c6518dd8edc0b1624b4e2b6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940290"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>IContextNode::CreatePartiallyPopulatedSubNode-Methode

Erstellt ein untergeordnetes [**IContextNode-Objekt,**](icontextnode.md) das nur Informationen zu Typ, Bezeichner und Speicherort enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNodeType* \[ In\]
</dt> <dd>

Der Typ des zu erstellende Kontextknotens.

</dd> <dt>

*pNodeId* \[ In\]
</dt> <dd>

Der Bezeichner für den neuen Knoten.

</dd> <dt>

*pNodeLocation* \[ In\]
</dt> <dd>

Der Speicherort des neuen Knotens.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ out\]
</dt> <dd>

Ein Zeiger auf den neuen, teilweise aufgefüllten [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *pPartiallyPopulatedContextNodeCreated* auf, wenn Sie den Kontextknoten nicht mehr verwenden müssen.

 

Der neue [**IContextNode**](icontextnode.md) wird der Auflistung der untergeordneten Knoten dieses Kontextknotens hinzugefügt (siehe [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Wenn vorhandene untergeordnete Knoten vorhanden sind, wird der neu erstellte **IContextNode** als letzter untergeordneter Knoten hinzugefügt.

Weitere Informationen zu Typ, Bezeichner und Speicherort finden Sie unter [**IContextNode::GetType,**](icontextnode-gettype.md) [**IContextNode::GetId**](icontextnode-getid.md)und [**IContextNode::GetLocation.**](icontextnode-getlocation.md)

Diese Methode wird für den Datenproxy verwendet, um ein [**IContextNode-Objekt**](icontextnode.md) in der Kontextknotenstruktur zu erstellen, bevor alle Informationen dazu verfügbar sind. Weitere Informationen finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Kontextknotentypen](context-node-types.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

