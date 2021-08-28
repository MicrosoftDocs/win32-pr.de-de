---
description: 'CBasePin.Inactive-Methode: Die Inactive-Methode benachrichtigt den Pin darüber, dass der Filter nicht mehr aktiv ist.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: CBasePin.Inactive-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052740"
---
# <a name="cbasepininactive-method"></a>CBasePin.Inactive-Methode

Die `Inactive` -Methode benachrichtigt den Pin, dass der Filter nicht mehr aktiv ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn der Filter beendet wird, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode für alle verbundenen Pins des Filters auf.

Diese Methode führt in der Basisklasse nichts aus. Abgeleitete Klassen sollten diese Methode überschreiben, um alle Von der [**CBasePin::Active-Methode**](cbasepin-active.md) abgerufenen Ressourcen freizusetzen. z. B. , um die Zuweisungen des Pins zu decommitisieren.

Der interne Zustand des Filtergraph-Managers wird erst aktualisiert, nachdem diese Methode zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




