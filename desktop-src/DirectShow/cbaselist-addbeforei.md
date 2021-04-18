---
description: Die addbeforei-Methode fügt ein Element vor der angegebenen Position ein.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Cbaselist. addbeforei-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365463"
---
# <a name="cbaselistaddbeforei-method"></a>Cbaselist. addbeforei-Methode

Die- `AddBeforeI` Methode fügt ein Element vor der angegebenen Position ein.

## <a name="syntax"></a>Syntax


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Die Position, vor der das Element hinzugefügt werden soll.

</dd> <dt>

*pobj* 
</dt> <dd>

Zeiger auf das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator für das eingefügte Element zurück.

## <a name="remarks"></a>Bemerkungen

Wenn *POS* **null** ist, fügt diese Methode das Element am Ende der Liste hinzu (entspricht dem Aufruf der [**cbaselist:: addtaili**](cbaselist-addtaili.md) -Methode).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




