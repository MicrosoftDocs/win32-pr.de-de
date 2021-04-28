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
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095987"
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

## <a name="remarks"></a>Bemerkungen

Diese Methode legt das Format für eine Stecknadelverbindung fest. Vor dem Aufrufen dieser Methode ruft der Pin die [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf, um zu bestimmen, ob der Medientyp akzeptabel ist. Daher wird angenommen, dass der *pmt-Parameter* ein zulässiger Medientyp ist.

In der Basisklasse legt diese Methode die [**CBasePin::m \_ mt-Membervariable**](cbasepin-m-mt.md) fest und gibt S \_ OK zurück. Eine abgeleitete Klasse kann diese Methode überschreiben, wenn sie eine Benachrichtigung erfordert, wenn der Medientyp festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




