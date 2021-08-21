---
description: Die AddTailI-Methode fügt am Ende der Liste ein Element hinzu.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: CBaseList.AddTailI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659126"
---
# <a name="cbaselistaddtaili-method"></a>CBaseList.AddTailI-Methode

Die `AddTailI` -Methode fügt am Ende der Liste ein Element hinzu.

## <a name="syntax"></a>Syntax


```C++
POSITION AddTailI(
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

Gibt einen POSITION-Wert für die neue Endposition zurück.

## <a name="remarks"></a>Hinweise

Wenn die Methode fehlschlägt, wird **NULL** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




