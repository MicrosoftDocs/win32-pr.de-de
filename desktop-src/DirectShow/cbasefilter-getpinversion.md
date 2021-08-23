---
description: Die GetPinVersion-Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: CBaseFilter.GetPinVersion-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a40890ce40e75ebea9f7dd10edb78572eb865ea5f94cd1ec674c082d6df8c631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640460"
---
# <a name="cbasefiltergetpinversion-method"></a>CBaseFilter.GetPinVersion-Methode

Die `GetPinVersion` -Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.

## <a name="syntax"></a>Syntax


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBaseFilter::m \_ PinVersion-Membervariable**](cbasefilter-m-pinversion.md) zurück.

## <a name="remarks"></a>Hinweise

Der **CBaseFilter-Konstruktor** initialisiert die Pin-Version auf 1. In der Basisklasse ändert sich diese Zahl nie. Wenn der Filter Pins dynamisch erstellt oder zerstört, sollte er die Pinversion erhöhen, sobald sich die Pins ändern. Um die Versionsnummer zu erhöhen, rufen Sie die [**CBaseFilter::IncrementPinVersion-Methode**](cbasefilter-incrementpinversion.md) auf.

Das pin-Enumeratorobjekt, das von der [**CEnumPins-Klasse**](cenumpins.md) implementiert wird, verwendet die Pinversion, um sich selbst mit dem Filter zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




