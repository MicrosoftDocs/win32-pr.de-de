---
description: 'Die get- \_ Raten Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaposition:: get- \_ Raten Methode.'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: CPosPassThru.get_Rate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360429"
---
# <a name="cpospassthruget_rate-method"></a>Cpospassthru. get- \_ Raten Methode

Die- `get_Rate` Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die [**imediaposition:: get- \_ Raten**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Rate(
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

 

 




