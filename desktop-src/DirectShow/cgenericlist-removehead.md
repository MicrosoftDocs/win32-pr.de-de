---
description: Die RemoveHead-Methode entfernt das erste Element in der Liste.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Cgenericlist. RemoveHead-Methode (wxlist. h)
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
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370191"
---
# <a name="cgenericlistremovehead-method"></a>Cgenericlist. RemoveHead-Methode

Die- `RemoveHead` Methode entfernt das erste Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) oder **null** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das der Knoten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cgenericlist-Klasse**](cgenericlist.md)
</dt> </dl>

 

 




