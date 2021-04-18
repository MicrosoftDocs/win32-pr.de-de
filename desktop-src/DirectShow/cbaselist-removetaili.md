---
description: Die removetaili-Methode entfernt das letzte Element in der Liste.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Cbaselist. removetaili-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371444"
---
# <a name="cbaselistremovetaili-method"></a>Cbaselist. removetaili-Methode

Die- `RemoveTailI` Methode entfernt das letzte Element in der Liste.

## <a name="syntax"></a>Syntax


```C++
void* RemoveTailI();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element oder **null** zurück, wenn die Liste leer ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das im Knoten enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




