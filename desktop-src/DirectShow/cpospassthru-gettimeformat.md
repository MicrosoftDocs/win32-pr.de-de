---
description: 'CPosPassThru.GetTimeFormat-Methode: Die GetTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die IMediaSeeking::GetTimeFormat-Methode.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: CPosPassThru.GetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e88be870839639c682fb653408736fcc505e6fef84edbc168555aeb462e6e387
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055120"
---
# <a name="cpospassthrugettimeformat-method"></a>CPosPassThru.GetTimeFormat-Methode

Die `GetTimeFormat` -Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die [**IMediaSeeking::GetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.

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
</dt> <dt>

[**GUIDs im Zeitformat**](time-format-guids.md)
</dt> </dl>

 

 




