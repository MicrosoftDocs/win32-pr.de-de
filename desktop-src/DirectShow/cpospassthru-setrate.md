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
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095218"
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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




