---
description: 'CBasePin.SetMediaType-Methode: Die SetMediaType-Methode legt den Medientyp für die Verbindung fest.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: CBasePin.SetMediaType-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e71047b5063a5975266e5e24db936a0baf9e7b65e81ce29b402ccce4638267a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108640"
---
# <a name="cbasepinsetmediatype-method"></a>CBasePin.SetMediaType-Methode

Die `SetMediaType` -Methode legt den Medientyp für die Verbindung fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pmt* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt das Format für eine Stecknadelverbindung fest. Vor dem Aufrufen dieser Methode ruft der Pin die [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf, um zu bestimmen, ob der Medientyp akzeptabel ist. Daher wird davon ausgegangen, dass der *pmt-Parameter* ein akzeptabler Medientyp ist.

In der Basisklasse legt diese Methode die [**CBasePin::m \_ mt-Membervariable**](cbasepin-m-mt.md) fest und gibt S \_ OK zurück. Eine abgeleitete Klasse kann diese Methode überschreiben, wenn sie eine Benachrichtigung erfordert, wenn der Medientyp festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




