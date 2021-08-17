---
description: Fügt ein Element in die Warteschlange ein.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: CQueue.PutQueueObject-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6e3539b12f81421e90de1f8311210aa2acb77173be2991bd6f15a1c84d39ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539010"
---
# <a name="cqueueputqueueobject-method"></a>CQueue.PutQueueObject-Methode

Fügt ein Element in die Warteschlange ein.

## <a name="syntax"></a>Syntax


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*object* 
</dt> <dd>

Objekt vom Typ **T** (Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird blockiert, bis speicherplatz in der Warteschlange für das Element vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CQueue-Klasse**](cqueue.md)
</dt> </dl>

 

 




