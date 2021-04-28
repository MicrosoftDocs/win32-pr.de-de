---
description: 'CPosPassThru.SetTimeFormat-Methode: Die SetTimeFormat-Methode legt das Zeitformat fest. Diese Methode implementiert die IMediaSeeking::SetTimeFormat-Methode.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: CPosPassThru.SetTimeFormat-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085468"
---
# <a name="cpospassthrusettimeformat-method"></a>CPosPassThru.SetTimeFormat-Methode

Die SetTimeFormat-Methode legt das Zeitformat fest. Diese Methode implementiert die [**IMediaSeeking::SetTimeFormat-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine GUID im Zeitformat.

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
</dt> <dt>

[**Zeitformat-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




