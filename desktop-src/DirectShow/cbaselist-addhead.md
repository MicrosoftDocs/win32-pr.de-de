---
description: Die AddHead-Methode fügt am Anfang dieser Liste eine andere Liste ein.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Cbaselist. AddHead-Methode (wxlist. h)
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
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373785"
---
# <a name="cbaselistaddhead-method"></a>Cbaselist. AddHead-Methode

Die- `AddHead` Methode fügt am Anfang dieser Liste eine andere Liste ein.

## <a name="syntax"></a>Syntax


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pList* 
</dt> <dd>

Ein Zeiger auf die Liste der hinzu zufügenden Elemente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, wurden möglicherweise einige Elemente zur Liste hinzugefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




