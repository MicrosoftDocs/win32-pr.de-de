---
description: 'CDynamicOutputPin.DeliverEndFlush-Methode: Die DeliverEndFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: CDynamicOutputPin.DeliverEndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095708"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>CDynamicOutputPin.DeliverEndFlush-Methode

Die `DeliverEndFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder einen **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::D eliverEndFlush-Methode.**](cbaseoutputpin-deliverendflush.md) Das Ereignis [**CDynamicOutputPin::m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) wird zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




