---
description: Die RemoveHead-Methode entfernt das erste Element in der Liste.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: CGenericList.RemoveHead-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b374ad6a08aac039de3c7d54ee4403f240fdf6bf9839a5ea2554901de789f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317750"
---
# <a name="cgenericlistremovehead-method"></a>CGenericList.RemoveHead-Methode

Die `RemoveHead` -Methode entfernt das erste Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ **OBJECT** (vorlagentyp) oder **NULL** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Hinweise

Diese Methode löscht den Listenknoten, aber nicht das Element, das der Knoten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CGenericList-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




