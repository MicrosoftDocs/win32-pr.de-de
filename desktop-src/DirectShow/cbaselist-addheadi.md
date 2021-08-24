---
description: Die AddHeadI-Methode fügt am Ende der Liste ein Element hinzu.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: CBaseList.AddHeadI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c1f22434aa2c927933c36ec496d5880ca8f3f673b314d7a8197079203757427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568120"
---
# <a name="cbaselistaddheadi-method"></a>CBaseList.AddHeadI-Methode

Die `AddHeadI` -Methode fügt am Ende der Liste ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObj* 
</dt> <dd>

Zeiger auf das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen POSITION-Wert zurück, der die neue Kopfposition angibt.

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, ist der Rückgabewert **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




