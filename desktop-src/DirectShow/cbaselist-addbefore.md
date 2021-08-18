---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: CBaseList.AddBefore-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4f85536b6a9372f164f596f96758a503096dbb0a5e5ed55adab42bc406b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016968"
---
# <a name="cbaselistaddbefore-method"></a>CBaseList.AddBefore-Methode

Die `AddBefore` -Methode fügt eine Liste vor der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Position, vor der die Liste eingefügt werden soll.

</dd> <dt>

*Plist* 
</dt> <dd>

Zeiger auf die hinzuzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Vorhandene Positionsindikatoren, einschließlich der im *pos-Parameter* angegebenen, bleiben gültig. Wenn bei der Methode ein Fehler auftritt, wurden möglicherweise einige Elemente hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




