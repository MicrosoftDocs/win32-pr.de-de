---
description: 'Die setTime-Methode legt die streamzeiten fest, wenn dieses Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die imediasample:: setTime-Methode.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Cmediasample. setTime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365155"
---
# <a name="cmediasamplesettime-method"></a>Cmediasample. setTime-Methode

Die- `SetTime` Methode legt die streamzeiten fest, wenn dieses Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimestart* 
</dt> <dd>

Zeiger auf die streamzeit, zu der das Beispiel beginnt, in 100-Nanosecond-Einheiten oder **null**.

</dd> <dt>

*ptimeend* 
</dt> <dd>

Zeiger auf die streamzeit, zu der das Beispiel endet, in 100-Nanosecond-Einheiten oder **null**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode legt die Endelement Variablen [**cmediasample:: m \_ Start**](cmediasample-m-start.md) und [**cmediasample \_ :: m**](cmediasample-m-end.md) fest, mit denen die Zeitstempel angegeben werden. Außerdem wird die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) aktualisiert, die angibt, ob die Zeitstempel gültig sind.

Weitere Informationen zu Zeitstempeln finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




