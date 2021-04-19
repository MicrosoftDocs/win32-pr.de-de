---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Crenderedinputpin. endflush-Methode (amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d80f6cbc31a8bc5bf797847465a218f32631c1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368485"
---
# <a name="crenderedinputpinendflush-method"></a>Crenderedinputpin. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang. Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht alle ausstehenden [**EC \_ Complete**](ec-complete.md) -Ereignisse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crenderedinputpin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




