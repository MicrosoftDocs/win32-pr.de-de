---
description: Die Duration-Methode ruft die Dauer des Streams ab.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: CPullPin.Duration-Methode (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdc944400bc80fbd5228ac06e2ba1c01f7315305071f7a24c0b38eb125ee1399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767980"
---
# <a name="cpullpinduration-method"></a>CPullPin.Duration-Methode

Die `Duration` -Methode ruft die Dauer des Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptDuration* 
</dt> <dd>

Zeiger auf eine Variable, die die Dauer empfängt, in Bytes multipliziert mit 10.000.000.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Dauer ist unbestimmt, bis die [**CPullPin::Verbinden-Methode**](cpullpin-connect.md) aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




