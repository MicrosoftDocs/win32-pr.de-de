---
description: 'Die getrate-Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaseeking:: getrate-Methode.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Cpospassthru. getrate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366911"
---
# <a name="cpospassthrugetrate-method"></a>Cpospassthru. getrate-Methode

Die- `GetRate` Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die [**imediaseeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdrate* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Wiedergabe Rate empfängt.

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

 

 




