---
description: Fügt ein Element in die Warteschlange ein.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Cqueue. putqueueobject-Methode (wxutil. h)
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
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361412"
---
# <a name="cqueueputqueueobject-method"></a>Cqueue. putqueueobject-Methode

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

Ein Objekt vom Typ **T** (der Vorlagentyp).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird blockiert, bis der Speicherplatz in der Warteschlange für das Element vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqueue-Klasse**](cqueue.md)
</dt> </dl>

 

 




