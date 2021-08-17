---
description: Die IncremementPinVersion-Methode erhöht die Versionsnummer für den Satz von Stecknadeln.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: CBaseFilter.IncrementPinVersion-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01c82a5f506673b6145b468004bbc900d3acdb051f525df20930344137618e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824108"
---
# <a name="cbasefilterincrementpinversion-method"></a>CBaseFilter.IncrementPinVersion-Methode

Die `IncremementPinVersion` -Methode erhöht die Versionsnummer für den Satz von Stecknadeln.

## <a name="syntax"></a>Syntax


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erhöht die [**CBaseFilter::m \_ PinVersion-Membervariable.**](cbasefilter-m-pinversion.md) Wenn der Filter Pins dynamisch erstellt oder zerstört, rufen Sie diese Methode auf, wenn sich die Stecknadeln ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> <dt>

[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




