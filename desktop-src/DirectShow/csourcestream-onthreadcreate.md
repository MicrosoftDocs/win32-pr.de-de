---
description: Die OnThreadCreate-Methode wird aufgerufen, wenn der Streamingthread initialisiert wird.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: CSourceStream.OnThreadCreate-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e263f0ae72838504ab6d219c71d7841291a3edd2a7d6b719d112c74fb30c23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907710"
---
# <a name="csourcestreamonthreadcreate-method"></a>CSourceStream.OnThreadCreate-Methode

Die `OnThreadCreate` -Methode wird aufgerufen, wenn der Streamingthread initialisiert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die Threadprozedur [**CSourceStream::ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, wenn sie zum ersten Mal eine [**CSourceStream::Init-Anforderung**](csourcestream-init.md) empfängt. Die -Methode führt in der Basisklasse nichts aus. Die abgeleitete Klasse kann diese Methode überschreiben, um Threadin initialisierungen durchzuführen. Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




