---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode überschreibt die ctransformfilter:: endflush-Methode.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Cvideotransformfilter. endflush-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359662"
---
# <a name="cvideotransformfilterendflush-method"></a>Cvideotransformfilter. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang. Diese Methode überschreibt die [**ctransformfilter:: endflush**](ctransformfilter-endflush.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode setzt alle internen Leistungsmessungen des Filters zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




