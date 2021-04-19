---
description: Die removeheadi-Methode entfernt das erste Element in der Liste.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Cbaselist. removeheadi-Methode (wxlist. h)
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
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368641"
---
# <a name="cbaselistremoveheadi-method"></a>Cbaselist. removeheadi-Methode

Die- `RemoveHeadI` Methode entfernt das erste Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element oder **null** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das der Knoten enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




