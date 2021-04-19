---
description: Die Put \_ Rate-Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die imediaposition::p UT- \_ Raten Methode.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: CPosPassThru.put_Rate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369366"
---
# <a name="cpospassthruput_rate-method"></a>Cpospassthru. Put \_ Rate-Methode

Die- `put_Rate` Methode legt die Wiedergabe Rate fest. Diese Methode implementiert die [**imediaposition::p UT- \_ Raten**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*drate* 
</dt> <dd>

Wiedergabe Rate. Darf nicht NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ invalidArg zurück, wenn *drate* 0 (null) ist. Andernfalls wird der **HRESULT** -Wert aus der verbundenen Pin zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Negative Raten weisen auf die umgekehrte Wiedergabe hin. Nicht alle Medien unterstützen die umgekehrte Wiedergabe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




