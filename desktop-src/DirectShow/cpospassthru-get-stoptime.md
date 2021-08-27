---
description: Die get StopTime-Methode ruft den Zeitpunkt ab, zu dem die Wiedergabe relativ \_ zur Dauer des Streams stoppt. Diese Methode implementiert die IMediaPosition::get \_ StopTime-Methode.
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: CPosPassThru.get_StopTime -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea233d7e3a148088edd0f6963f45aeb0b483b41317481a95733fdc73c242027d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108300"
---
# <a name="cpospassthruget_stoptime-method"></a>CPosPassThru.get \_ StopTime-Methode

Die -Methode ruft den Zeitpunkt ab, zu dem die `get_StopTime` Wiedergabe relativ zur Dauer des Streams anzuhalten ist. Diese Methode implementiert die [**IMediaPosition::get \_ StopTime-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pllTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Sekunden empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




