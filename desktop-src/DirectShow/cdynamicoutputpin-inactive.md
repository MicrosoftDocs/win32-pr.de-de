---
description: Die inaktive Methode benachrichtigt den Stecknadel, dass der Filter beendet wurde.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: CDynamicOutputPin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d52ec1735be6d4e89885295a9d9c2d382142fdc9d31f95b6368d0ef2f331608e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317710"
---
# <a name="cdynamicoutputpininactive-method"></a>CDynamicOutputPin.Inactive-Methode

Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter beendet wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseOutputPin::Inactive-Methode.**](cbaseoutputpin-inactive.md) Es legt das [**CDynamicOutputPin::m \_ hStopEvent-Ereignis**](cdynamicoutputpin-m-hstopevent.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




