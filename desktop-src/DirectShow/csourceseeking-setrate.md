---
description: 'CSourceSeeking.SetRate-Methode: Die SetRate-Methode legt die Wiedergaberate fest. Diese Methode implementiert die IMediaSeeking::SetRate-Methode.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: CSourceSeeking.SetRate-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098738"
---
# <a name="csourceseekingsetrate-method"></a>CSourceSeeking.SetRate-Methode

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

Wiedergaberate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode aktualisiert den Wert der [**CSourceSeeking::m \_ dRateSeeking-Membervariablen**](csourceseeking-m-drateseeking.md) und ruft dann die reine virtuelle Methode [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)auf. Die -Methode überprüft den *dRate-Parameter* nicht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




