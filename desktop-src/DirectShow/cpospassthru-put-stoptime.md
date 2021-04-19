---
description: Die Put \_ stopTime-Methode legt die Zeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die imediaposition::p UT \_ stopTime-Methode.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: CPosPassThru.put_StopTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371550"
---
# <a name="cpospassthruput_stoptime-method"></a>Cpospassthru. Put \_ stopTime-Methode

Die- `put_StopTime` Methode legt die Uhrzeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die [**imediaposition::p UT \_ stopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lltime* 
</dt> <dd>

Endzeit als **Double** -Wert in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




