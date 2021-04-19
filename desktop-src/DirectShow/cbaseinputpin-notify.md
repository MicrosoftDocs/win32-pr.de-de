---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Cbasonputpin. Notify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358679"
---
# <a name="cbaseinputpinnotify-method"></a>Cbasinput PIN. Notify-Methode

Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pself* 
</dt> <dd>

Zeiger auf den Filter, der die Qualitäts Steuerungs Meldung sendet.

</dd> <dt>

*Q1* 
</dt> <dd>

[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Filter übergeben in der Regel Qualitäts Steuerungs Meldungen an eine upstreamausgabepin und nicht an eine Eingabe-PIN. Daher gibt diese Methode S OK zurück, \_ ohne etwas zu tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> <dt>

[Qualitäts Steuerungs Verwaltung](quality-control-management.md)
</dt> </dl>

 

 




