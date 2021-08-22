---
description: Die put \_ Rate-Methode legt die Wiedergaberate fest. Diese Methode implementiert die IMediaPosition::p \_ Rate-Methode.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: CPosPassThru.put_Rate -Methode (Ctlutil.h)
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
ms.openlocfilehash: 90c89c9730ee057bea3bc776f551061c0e828385fe3c6ae054f4161bdb705ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565501"
---
# <a name="cpospassthruput_rate-method"></a>CPosPassThru.put \_ Rate-Methode

Die `put_Rate` -Methode legt die Wiedergaberate fest. Diese Methode implementiert die [**IMediaPosition::p ut \_ Rate-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate)

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dRate* 
</dt> <dd>

Wiedergaberate. Darf nicht 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ INVALIDARG zurück, wenn *dRate* 0 (null) ist. Andernfalls wird der **HRESULT-Wert** vom verbundenen Pin zurückgegeben.

## <a name="remarks"></a>Hinweise

Negative Raten geben reverse play an. Nicht alle Medien unterstützen reverseplay.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




