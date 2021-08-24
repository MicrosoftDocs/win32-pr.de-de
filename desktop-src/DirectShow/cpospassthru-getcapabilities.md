---
description: 'CPosPassThru.GetCapabilities-Methode: Die GetCapabilities-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die IMediaSeeking::GetCapabilities-Methode.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: CPosPassThru.GetCapabilities-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3f9c47022ece0305e3111fe21f365544ed495cfe3c1343b908309f801a1a0b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073543"
---
# <a name="cpospassthrugetcapabilities-method"></a>CPosPassThru.GetCapabilities-Methode

Die **GetCapabilities-Methode** ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die [**IMediaSeeking::GetCapabilities-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Zeiger auf eine Variable, die eine bitweise Kombination von [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES-Flags**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




