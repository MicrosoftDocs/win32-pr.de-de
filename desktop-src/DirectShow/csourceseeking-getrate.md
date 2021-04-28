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
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085228"
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



 

## <a name="remarks"></a>Bemerkungen

Die Wiedergaberate wird durch die [**Membervariable CSourceSeeking::m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




