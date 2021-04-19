---
description: Die onthreadcreate-Methode wird aufgerufen, wenn der streamingindthread initialisiert wird.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Csourcestream. onthreadcreate-Methode (Source. h)
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
ms.openlocfilehash: a5ae3c210ca81eafa1951fc51301eaf50491357f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370208"
---
# <a name="csourcestreamonthreadcreate-method"></a>Csourcestream. onthreadcreate-Methode

Die- `OnThreadCreate` Methode wird aufgerufen, wenn der streamingthread initialisiert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Thread Prozedur [**csourcestream:: ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, wenn Sie zum ersten Mal eine [**csourcestream:: init**](csourcestream-init.md) -Anforderung empfängt. Die-Methode führt in der-Basisklasse keine Aktion aus. Die abgeleitete Klasse kann diese Methode überschreiben, um Thread Initialisierungen auszuführen. Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




