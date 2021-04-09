---
description: Erstellt ein untergeordnetes icontextnode-Objekt, das nur Informationen über Typ, Bezeichner und Speicherort enthält.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Icontextnode:: kreatepartiallypopulatedsubnode-Methode (iacom. h)'
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
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862723"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Icontextnode:: kreatepartiallypopulatedsubnode-Methode

Erstellt ein untergeordnetes [**icontextnode**](icontextnode.md) -Objekt, das nur Informationen über Typ, Bezeichner und Speicherort enthält.

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

*pnodetype* \[ in\]
</dt> <dd>

Der Typ des zu erstellenden Kontext Knotens.

</dd> <dt>

*pnodeid* \[ in\]
</dt> <dd>

Der Bezeichner für den neuen Knoten.

</dd> <dt>

*pnodelokation* \[ in\]
</dt> <dd>

Der Speicherort des neuen Knotens.

</dd> <dt>

*ppartiallypopulatedcontextnode created* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den neuen, teilweise aufgefüllten [**icontextnode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speichermangel zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *ppartiallypopulatedcontextnodecreated* aufrufen, wenn Sie den Kontext Knoten nicht mehr verwenden müssen.

 

Der neue [**icontextnode**](icontextnode.md) wird der Auflistung von untergeordneten Knoten dieses Kontext Knotens hinzugefügt (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)). Wenn vorhandene untergeordnete Knoten vorhanden sind, wird der neu erstellte **icontextnode** als letzter untergeordneter Knoten hinzugefügt.

Weitere Informationen zu Typ, Bezeichner und Speicherort finden Sie unter [**icontextnode:: GetType**](icontextnode-gettype.md), [**icontextnode:: GetId**](icontextnode-getid.md)und [**icontextnode:: getLocation**](icontextnode-getlocation.md).

Diese Methode wird für Daten Proxys als Möglichkeit zum Erstellen eines [**icontextnode**](icontextnode.md) -Objekts in der Kontext Knoten Struktur verwendet, bevor alle Informationen über diese verfügbar sind. Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

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

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

