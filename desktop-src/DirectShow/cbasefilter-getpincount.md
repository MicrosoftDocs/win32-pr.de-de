---
description: Die getpincount-Methode ruft die Anzahl der Pins ab.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Cbasefilter. getpincount-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366842"
---
# <a name="cbasefiltergetpincount-method"></a>Cbasefilter. getpincount-Methode

Die- `GetPinCount` Methode ruft die Anzahl der Pins ab.

## <a name="syntax"></a>Syntax


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Pins zurück.

## <a name="remarks"></a>Bemerkungen

Diese reine virtuelle Methode muss von der abgeleiteten Klasse implementiert werden. Gibt die Anzahl der Pins zurück, die zurzeit für diesen Filter verfügbar sind. Filter können Pins dynamisch erstellen oder zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




