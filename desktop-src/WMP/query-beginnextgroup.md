---
title: Query.beginNextGroup-Methode
description: Die beginNextGroup-Methode beginnt eine neue Bedingungsgruppe. | Query.beginNextGroup-Methode
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- beginNextGroup-Windows Media Player
- beginNextGroup-Methode Windows Media Player , Query-Klasse
- Abfrageklasse Windows Media Player , beginNextGroup-Methode
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d12f8e37c32b83afb3e518deda09643033c7f396d8c52a2898893a01dc930d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861850"
---
# <a name="querybeginnextgroup-method"></a>Query.beginNextGroup-Methode

Die **beginNextGroup-Methode** beginnt eine neue Bedingungsgruppe.

## <a name="syntax"></a>Syntax


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Beginnen einer neuen Bedingungsgruppe impliziert, dass Sie die aktuelle Bedingungsgruppe abgeschlossen haben. Die neue Bedingungsgruppe wird immer mithilfe der OR-Logik mit der vorherigen Bedingungsgruppe verkettet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Abfrageobjekt**](query-object.md)
</dt> <dt>

[**Query.addCondition**](query-addcondition.md)
</dt> </dl>

 

 





