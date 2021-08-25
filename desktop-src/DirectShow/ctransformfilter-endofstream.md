---
description: Die EndOfStream-Methode benachrichtigt den Filter, dass keine zusätzlichen Daten vom Eingabepin erwartet werden.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: CTransformFilter.EndOfStream-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907630"
---
# <a name="ctransformfilterendofstream-method"></a>CTransformFilter.EndOfStream-Methode

Die `EndOfStream` -Methode benachrichtigt den Filter, dass keine zusätzlichen Daten vom Eingabepin erwartet werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Die [**CTransformInputPin::EndOfStream-Methode**](ctransforminputpin-endofstream.md) des Eingabepins ruft diese Methode auf. Diese Methode stellt die End-of-Stream-Benachrichtigung nachgeschaltet zur Verfügung. Wenn die abgeleitete Klasse einen Arbeitsthread zum Senden von Medienbeispielen verwendet, sollte sie diese Methode überschreiben und die Benachrichtigung zum Streamende in die Warteschlange stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




