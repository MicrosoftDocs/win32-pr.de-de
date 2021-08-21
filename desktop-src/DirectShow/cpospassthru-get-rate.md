---
description: Die Get \_ Rate-Methode ruft die Wiedergaberate ab. Diese Methode implementiert die IMediaPosition::get \_ Rate-Methode.
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: CPosPassThru.get_Rate-Methode (Ctlutil.h)
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
ms.openlocfilehash: 4fa8014d23bc488b4f0b8b0cc9b872dfdf4a56cced396cc22eefab5912df1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073535"
---
# <a name="cpospassthruget_rate-method"></a>CPosPassThru.get \_ Rate-Methode

Die `get_Rate` -Methode ruft die Wiedergaberate ab. Diese Methode implementiert die [**IMediaPosition::get \_ Rate-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Rate(
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



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




