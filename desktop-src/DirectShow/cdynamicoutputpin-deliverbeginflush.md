---
description: 'CDynamicOutputPin.DeliverBeginFlush-Methode: Die DeliverBeginFlush-Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: CDynamicOutputPin.DeliverBeginFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099318"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>CDynamicOutputPin.DeliverBeginFlush-Methode

Die `DeliverBeginFlush` -Methode fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder einen **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CBaseOutputPin::D eliverBeginFlush-Methode.**](cbaseoutputpin-deliverbeginflush.md) Es legt das [**CDynamicOutputPin::m \_ hStopEvent-Ereignis**](cdynamicoutputpin-m-hstopevent.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




