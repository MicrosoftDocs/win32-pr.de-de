---
description: Die RemoveHeadI-Methode entfernt das erste Element in der Liste.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: CBaseList.RemoveHeadI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc4d9e039735888d6694422a1802b73b3781316210fd42e13eec9bac5094d322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814310"
---
# <a name="cbaselistremoveheadi-method"></a>CBaseList.RemoveHeadI-Methode

Die `RemoveHeadI` -Methode entfernt das erste Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element oder **NULL zurück,** wenn die Liste leer ist.

## <a name="remarks"></a>Hinweise

Diese Methode löscht den Listenknoten, aber nicht das Element, das der Knoten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




