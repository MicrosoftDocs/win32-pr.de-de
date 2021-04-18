---
description: Die incremementpinversion-Methode erhöht die Versionsnummer für den Satz von Pins.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Cbasefilter. incrementpinversion-Methode (amfilter. h)
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
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372672"
---
# <a name="cbasefilterincrementpinversion-method"></a>Cbasefilter. incrementpinversion-Methode

Die- `IncremementPinVersion` Methode erhöht die Versionsnummer für den Satz von Pins.

## <a name="syntax"></a>Syntax


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht die Member-Variable [**cbasefilter:: m \_ pinversion**](cbasefilter-m-pinversion.md) . Wenn der Filter Pins dynamisch erstellt oder zerstört, wird diese Methode immer dann aufgerufen, wenn die Pins geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> <dt>

[**Cbasefilter:: getpinversion**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




