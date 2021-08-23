---
description: Die AddHead-Methode fügt eine weitere Liste am Anfang dieser Liste ein.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: CBaseList.AddHead-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814320"
---
# <a name="cbaselistaddhead-method"></a>CBaseList.AddHead-Methode

Die `AddHead` -Methode fügt eine weitere Liste am Anfang dieser Liste ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Plist* 
</dt> <dd>

Zeiger auf die Liste der hinzuzufügende Elemente.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




