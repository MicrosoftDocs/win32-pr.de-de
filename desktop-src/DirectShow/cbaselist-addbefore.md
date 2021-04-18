---
description: Die AddBefore-Methode fügt eine Liste vor der angegebenen Position ein.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Cbaselist. AddBefore-Methode (wxlist. h)
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
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372415"
---
# <a name="cbaselistaddbefore-method"></a>Cbaselist. AddBefore-Methode

Die- `AddBefore` Methode fügt eine Liste vor der angegebenen Position ein.

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

Die Position, an der die Liste eingefügt werden soll.

</dd> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die einzufügende Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Vorhandene positionsindikatoren, einschließlich der im *POS* -Parameter angegebenen, bleiben gültig. Wenn die Methode fehlschlägt, wurden möglicherweise einige der Elemente hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




