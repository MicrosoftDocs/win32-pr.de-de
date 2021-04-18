---
description: Die addtaili-Methode fügt ein Element am Ende der Liste hinzu.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Cbaselist. addtaili-Methode (wxlist. h)
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
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361378"
---
# <a name="cbaselistaddtaili-method"></a>Cbaselist. addtaili-Methode

Die- `AddTailI` Methode fügt ein Element am Ende der Liste hinzu.

## <a name="syntax"></a>Syntax


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobj* 
</dt> <dd>

Zeiger auf das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Positionswert für die neue Endposition zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, wird **null** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




