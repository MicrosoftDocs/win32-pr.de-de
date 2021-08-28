---
description: Die GetI-Methode ruft das Element an der angegebenen Position ab.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: CBaseList.GetI-Methode (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087440"
---
# <a name="cbaselistgeti-method"></a>CBaseList.GetI-Methode

Die `GetI` -Methode ruft das Element an der angegebenen Position ab.

## <a name="syntax"></a>Syntax


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pos* 
</dt> <dd>

Positionsindikator für das abzurufende Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf das Element zurück.

## <a name="remarks"></a>Hinweise

Wenn *pos* **NULL** ist, gibt die Methode **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseList-Klasse**](cbaselist.md)
</dt> </dl>

 

 




