---
description: Die GetPinCount-Methode ruft die Anzahl der Pins im Filter ab.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: CTransformFilter.GetPinCount-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9269149d7f2bbc95e811515f70aa279a4aafd8cf34b2d5077ed69019b86c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953599"
---
# <a name="ctransformfiltergetpincount-method"></a>CTransformFilter.GetPinCount-Methode

Die `GetPinCount` -Methode ruft die Anzahl der Pins im Filter ab.

## <a name="syntax"></a>Syntax


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 2 zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseFilter::GetPinCount-Methode.**](cbasefilter-getpincount.md) Die **CTransformFilter-Klasse** unterstützt genau einen Eingabe- und einen Ausgabepin.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




