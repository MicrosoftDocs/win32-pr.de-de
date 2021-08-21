---
description: Die OnThreadDestroy-Methode wird aufgerufen, wenn der Streamingthread beendet wird.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: CSourceStream.OnThreadDestroy-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953699"
---
# <a name="csourcestreamonthreaddestroy-method"></a>CSourceStream.OnThreadDestroy-Methode

Die `OnThreadDestroy` -Methode wird aufgerufen, wenn der Streamingthread beendet wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Threadprozedur [**CSourceStream::ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, bevor sie beendet wird. Die -Methode führt in der Basisklasse nichts aus. sie ist für die abgeleitete Klasse zum Überschreiben verfügbar. Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




