---
description: 'Die settimeformat-Methode legt das Zeitformat fest. Diese Methode implementiert die imediaseeking:: settimeformat-Methode.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Cpospassthru. settimeformat-Methode (ctlutil. h)
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
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373773"
---
# <a name="cpospassthrusettimeformat-method"></a>Cpospassthru. settimeformat-Methode

Die settimeformat-Methode legt das Zeitformat fest. Diese Methode implementiert die [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Zeiger auf eine Zeitformat-GUID.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeit Format-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




