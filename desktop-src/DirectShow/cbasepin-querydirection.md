---
description: 'Die querydirection-Methode ruft die Richtung der PIN (Eingabe oder Ausgabe) ab. Diese Methode implementiert die IPin:: querydirection-Methode.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Cbasepin. querydirection-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370705"
---
# <a name="cbasepinquerydirection-method"></a>Cbasepin. querydirection-Methode

Die- `QueryDirection` Methode ruft die Richtung der PIN (Eingabe oder Ausgabe) ab. Diese Methode implementiert die [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppindir* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Member des enumerierten Typs der [**Pin- \_ Richtung**](/windows/win32/api/strmif/ne-strmif-pin_direction) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




