---
description: Die AddTail-Methode fügt eine weitere Liste an das Ende dieser Liste an.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: CBaseList.AddTail-Methode (Wxlist.h)
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
ms.openlocfilehash: 5663a69d803def2b37f9a1ba677966a5b26a8bfc6f7b6eb1eb98eef85bcd961d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659153"
---
# <a name="cbaselistaddtail-method"></a>CBaseList.AddTail-Methode

Die `AddTail` -Methode fügt eine weitere Liste an das Ende dieser Liste an.

## <a name="syntax"></a>Syntax


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plist* 
</dt> <dd>

Zeiger auf die anzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, wurden der Liste möglicherweise einige Elemente hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




