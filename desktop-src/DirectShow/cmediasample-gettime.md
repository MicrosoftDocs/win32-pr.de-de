---
description: 'Die getTime-Methode ruft die streamzeiten ab, zu denen das Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die imediasample:: getTime-Methode.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Cmediasample. getTime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354033"
---
# <a name="cmediasamplegettime-method"></a>Cmediasample. getTime-Methode

Die- `GetTime` Methode ruft die streamzeiten ab, zu denen das Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimestart* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die beginnende streamzeit in 100-Nanosecond-Einheiten empfängt.

</dd> <dt>

*ptimeend* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die endstreamzeit in 100-Nanosecond-Einheiten empfängt. Wenn das Beispiel keine Endzeit hat, wird der Wert auf die Startzeit plus 1 festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                   | Beschreibung                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Erfolg.<br/>                                         |
| <dl> <dt>**VFW \_ S \_ keine \_ \_ Endzeit**</dt> </dl>         | Sample hat eine gültige Startzeit, aber keine Endzeit.<br/> |
| <dl> <dt>**VFW \_ E- \_ Beispiel \_ Zeit \_ nicht \_ festgelegt**</dt> </dl> | Das Beispiel enthält keine gültigen Zeitstempel.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Die endmember-Variablen " [**cmediasample:: m \_ Start**](cmediasample-m-start.md) " und " [**cmediasample:: m \_**](cmediasample-m-end.md) " geben die Zeitstempel an. Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt an, ob die Zeitstempel gültig sind.

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

 

 




