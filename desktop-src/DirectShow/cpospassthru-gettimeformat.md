---
description: 'Die getTimeFormat-Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die imediaseeking:: getTimeFormat-Methode.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Cpospassthru. getTimeFormat-Methode (ctlutil. h)
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
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362146"
---
# <a name="cpospassthrugettimeformat-method"></a>Cpospassthru. getTimeFormat-Methode

Die- `GetTimeFormat` Methode ruft das aktuelle Zeitformat ab. Diese Methode implementiert die [**imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt.

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

 

 




