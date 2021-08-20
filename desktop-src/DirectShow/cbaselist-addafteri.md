---
description: Die AddAfterI-Methode fügt ein Element nach der angegebenen Position ein.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: CBaseList.AddAfterI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b72be7342e6085b773ef2493f5ad138f73349dffcdafc1a60a380692df3f16ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016988"
---
# <a name="cbaselistaddafteri-method"></a>CBaseList.AddAfterI-Methode

Die `AddAfterI` -Methode fügt ein Element nach der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Position, nach der das Element hinzugefügt werden soll.

</dd> <dt>

*pObj* 
</dt> <dd>

Zeiger auf das hinzuzufügende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator des eingefügten Elements zurück.

## <a name="remarks"></a>Hinweise

Wenn *pos* **NULL** ist, fügt diese Methode das Element dem Kopf der Liste hinzu (entspricht dem Aufruf der [**CBaseList::AddHeadI-Methode).**](cbaselist-addheadi.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




