---
description: Die addheadi-Methode fügt ein Element am Anfang der Liste hinzu.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Cbaselist. addheadi-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370117"
---
# <a name="cbaselistaddheadi-method"></a>Cbaselist. addheadi-Methode

Mit der- `AddHeadI` Methode wird ein Element am Anfang der Liste hinzugefügt.

## <a name="syntax"></a>Syntax


```C++
POSITION AddHeadI(
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

Gibt einen Positionswert zurück, der die neue Head-Position angibt.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




