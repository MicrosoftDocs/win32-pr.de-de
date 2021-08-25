---
description: 'CSourceSeeking.GetRate-Methode: Die GetRate-Methode ruft die Wiedergaberate ab. Diese Methode implementiert die IMediaSeeking::GetRate-Methode.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: CSourceSeeking.GetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b734a5fafba9e38abbe853a8f3592a212130bf9a68de0efe7125aeea0ea01b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083950"
---
# <a name="csourceseekinggetrate-method"></a>CSourceSeeking.GetRate-Methode

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

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

## <a name="remarks"></a>Hinweise

Die Wiedergaberate wird durch die [**Membervariable CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




