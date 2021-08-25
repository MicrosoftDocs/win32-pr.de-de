---
description: Die MoveToHead-Methode teilt die Liste auf und fügt den Teil am Anfang einer anderen Liste ein.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: CBaseList.MoveToHead-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 18133107a3c8038780662bc39c8bd621c8b2c445a6e1e930f8fbfc015807e9fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928680"
---
# <a name="cbaselistmovetohead-method"></a>CBaseList.MoveToHead-Methode

Die `MoveToHead` -Methode teilt die Liste auf und fügt den Teil am Anfang einer anderen Liste ein.

## <a name="syntax"></a>Syntax


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionsindikator, der die Teilung in der Liste markiert.

</dd> <dt>

*Plist* 
</dt> <dd>

Zeiger auf eine andere Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode teilt die Liste vor der durch den *pos-Parameter* angegebenen Position auf. Der Hauptteil verbleibt in der Liste. Der Teil des Endes wird am Anfang der anderen Liste eingefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




