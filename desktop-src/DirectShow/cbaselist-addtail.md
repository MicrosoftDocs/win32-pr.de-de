---
description: Die AddTail-Methode fügt am Ende dieser Liste eine andere Liste an.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Cbaselist. AddTail-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356502"
---
# <a name="cbaselistaddtail-method"></a>Cbaselist. AddTail-Methode

Die- `AddTail` Methode fügt am Ende dieser Liste eine andere Liste an.

## <a name="syntax"></a>Syntax


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die anzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, wurden möglicherweise einige Elemente zur Liste hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




