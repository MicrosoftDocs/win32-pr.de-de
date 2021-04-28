---
description: 'CPosPassThru.GetRate-Methode: Die GetRate-Methode ruft die Wiedergaberate ab. Diese Methode implementiert die IMediaSeeking::GetRate-Methode.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: CPosPassThru.GetRate-Methode (Ctlutil.h)
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
ms.openlocfilehash: 997323ca2089a0b381b85c3730cb364d0883b1bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085558"
---
# <a name="cpospassthrugetrate-method"></a>CPosPassThru.GetRate-Methode

Die `GetRate` -Methode ruft die Wiedergaberate ab. Diese Methode implementiert die [**IMediaSeeking::GetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdRate* 
</dt> <dd>

Zeiger auf eine Variable, die die Wiedergaberate empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




