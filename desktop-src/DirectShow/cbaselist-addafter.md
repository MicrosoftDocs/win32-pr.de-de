---
description: Die AddAfter-Methode fügt eine Liste nach der angegebenen Position ein.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: CBaseList.AddAfter-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28351e1e0762b8e45bc9bf2ba1fe3624c67339e9b8bcf59ec5a919850a853061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983501"
---
# <a name="cbaselistaddafter-method"></a>CBaseList.AddAfter-Methode

Die `AddAfter` -Methode fügt eine Liste nach der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Position, nach der die Liste eingefügt werden soll.

</dd> <dt>

*Plist* 
</dt> <dd>

Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Vorhandene Positionsindikatoren, einschließlich der im *pos-Parameter* angegebenen, bleiben gültig. Wenn die Methode fehlschlägt, wurden möglicherweise einige der Elemente hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




