---
description: 'CBasePin.Active-Methode: Die Active-Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: CBasePin.Active-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1d651c58693789945af34d266aa8541679d1226d655530b90c542c8b0fc88b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872540"
---
# <a name="cbasepinactive-method"></a>CBasePin.Active-Methode

Die `Active` -Methode benachrichtigt den Pin, dass der Filter jetzt aktiv ist.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn der Filter von angehalten in angehalten wechselt, ruft die [**CBaseFilter-Klasse**](cbasefilter.md) diese Methode für alle verbundenen Pins des Filters auf.

Diese Methode führt in der Basisklasse nichts aus. Abgeleitete Klassen können diese Methode überschreiben. Beispielsweise kann ein Pin Zuweisungen committen oder Hardwareressourcen abrufen.

Der interne Zustand des Filtergraph-Managers wird erst aktualisiert, nachdem diese Memberfunktion zurückgegeben wurde. Testen Sie daher nicht den Zustand dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




