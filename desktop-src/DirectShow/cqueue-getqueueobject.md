---
description: Ruft das nächste Element aus der Warteschlange ab.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: CQueue.GetQueueObject-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108280"
---
# <a name="cqueuegetqueueobject-method"></a>CQueue.GetQueueObject-Methode

Ruft das nächste Element aus der Warteschlange ab.

## <a name="syntax"></a>Syntax


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Objekt vom Typ **T** (vorlagentyp) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode blockiert, bis ein Element in der Warteschlange verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CQueue-Klasse**](cqueue.md)
</dt> </dl>

 

 




