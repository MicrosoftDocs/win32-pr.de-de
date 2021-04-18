---
description: Die onthreaddestroy-Methode wird aufgerufen, wenn der streamingthread gerade beendet wird.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Csourcestream. onthreaddestroy-Methode (Quelle. h)
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
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358637"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Csourcestream. onthreaddestroy-Methode

Die- `OnThreadDestroy` Methode wird aufgerufen, wenn der streamingthread gerade beendet wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die Thread Prozedur [**csourcestream:: ThreadProc**](csourcestream-threadproc.md)ruft diese Methode auf, bevor Sie beendet wird. Die-Methode führt in der Basisklasse keine Aktion aus. Sie kann von der abgeleiteten Klasse außer Kraft gesetzt werden. Wenn die abgeleitete Klasse einen Fehlercode zurückgibt, wird der Thread mit einem Fehler beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




