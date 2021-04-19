---
description: Die addaf Teri-Methode fügt ein Element nach der angegebenen Position ein.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Cbaselist. addafteri-Methode (wxlist. h)
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
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370118"
---
# <a name="cbaselistaddafteri-method"></a>Cbaselist. addafteri-Methode

Die- `AddAfterI` Methode fügt ein Element nach der angegebenen Position ein.

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

Die Position, an der das Element hinzugefügt werden soll.

</dd> <dt>

*pobj* 
</dt> <dd>

Zeiger auf das hinzu zufügende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator des eingefügten Elements zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *POS* **null** ist, fügt diese Methode das Element am Anfang der Liste hinzu (entspricht dem Aufruf der [**cbaselist:: addheadi**](cbaselist-addheadi.md) -Methode).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




