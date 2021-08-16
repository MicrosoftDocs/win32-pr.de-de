---
description: Die AddBeforeI-Methode fügt ein Element vor der angegebenen Position ein.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: CBaseList.AddBeforeI-Methode (Wxlist.h)
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
ms.openlocfilehash: cfb995e614904e807e67eeee9c0f344525fd701d039c596eb081b6ff3be4f078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823747"
---
# <a name="cbaselistaddbeforei-method"></a>CBaseList.AddBeforeI-Methode

Die `AddBeforeI` -Methode fügt ein Element vor der angegebenen Position ein.

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

Position, vor der das Element hinzugefügt werden soll.

</dd> <dt>

*pObj* 
</dt> <dd>

Zeiger auf das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Positionsindikator für das eingefügte Element zurück.

## <a name="remarks"></a>Hinweise

Wenn *pos* **NULL** ist, fügt diese Methode das Element am Ende der Liste hinzu (entspricht dem Aufruf der [**CBaseList::AddTailI-Methode).**](cbaselist-addtaili.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




