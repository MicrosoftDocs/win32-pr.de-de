---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode implementiert die IPin:: endflush-Methode.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Cbaseoutputpin. endflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367772"
---
# <a name="cbaseoutputpinendflush-method"></a>Cbaseoutputpin. endflush-Methode

Die- `EndFlush` Methode beendet einen Löschvorgang. Diese Methode implementiert die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt "E unerwartete" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte nur für Eingabe Pins aufgerufen werden, sodass die **cbaseoutputpin** -Implementierung E \_ unerwartet zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




