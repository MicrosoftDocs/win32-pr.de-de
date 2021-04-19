---
description: Die-Methode wird von der-Methode der-Methode geteilt, und der Teil Fragment wird an der Spitze einer anderen Liste eingefügt.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Cbaselist. muvedehead-Methode (wxlist. h)
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
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361520"
---
# <a name="cbaselistmovetohead-method"></a>Cbaselist. muvedehead-Methode

Die `MoveToHead` -Methode teilt die Liste auf und fügt den Teil Fragment an der Spitze einer anderen Liste ein.

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

Positionsindikator, mit dem die Aufteilung in der Liste markiert wird.

</dd> <dt>

*pList* 
</dt> <dd>

Zeiger auf eine andere Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode teilt die Liste vor der durch den *POS* -Parameter angegebenen Position. Der Kopfteil verbleibt in der Liste. Der Teil Teil wird an der Spitze der anderen Liste eingefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




