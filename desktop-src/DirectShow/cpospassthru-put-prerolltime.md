---
description: Mit der Put \_ prerolltime-Methode wird die Datenmenge festgelegt, die vor der Startposition in die Warteschlange eingereiht wird. Diese Methode implementiert die imediaposition::p UT- \_ prerolltime-Methode.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: CPosPassThru.put_PrerollTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371622"
---
# <a name="cpospassthruput_prerolltime-method"></a>Cpospassthru. Put \_ prerolltime-Methode

Die- `put_PrerollTime` Methode legt die Menge der Daten fest, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die [**imediaposition::p UT- \_ prerolltime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lltime* 
</dt> <dd>

Vorab-Zeit in Sekunden.

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

 

 




