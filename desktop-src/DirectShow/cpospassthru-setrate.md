---
description: 'CPosPassThru.SetRate-Methode: Die SetRate-Methode legt die Wiedergaberate fest. Diese Methode implementiert die IMediaSeeking::SetRate-Methode.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: CPosPassThru.SetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c411f2c342bd54f89ac85ad4275a05e9d7854908c1d8ba88b1181f34e56f57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909070"
---
# <a name="cpospassthrusetrate-method"></a>CPosPassThru.SetRate-Methode

Die `SetRate` -Methode legt die Wiedergaberate fest. Diese Methode implementiert die [**IMediaSeeking::SetRate-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRate(
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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




