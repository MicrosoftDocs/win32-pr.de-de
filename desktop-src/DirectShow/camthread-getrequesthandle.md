---
description: Die GetRequestHandle-Methode ruft ein Handle für das Ereignis ab, das von der CABThread::CallWorker-Methode signalisiert wird.
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: CABThread.GetRequestHandle-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fa1be333ff35821f187cea980746c6b729a05c12e2103f4465bb44bbcc6f9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652590"
---
# <a name="camthreadgetrequesthandle-method"></a>CABThread.GetRequestHandle-Methode

Die `GetRequestHandle` -Methode ruft ein Handle für das -Ereignis ab, das von der [**CABThread::CallWorker-Methode**](camthread-callworker.md) signalisiert wird.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Ereignishandle zurück.

## <a name="remarks"></a>Hinweise

Die KLASSE CABEvent behält ein privates Ereignis für die manuelle Zurücksetzung bei, das von CallWorker festgelegt und von der [**METHODE "RESETThread::Reply"**](camthread-reply.md) zurückgesetzt wird.

Wenn Sie eine Funktion wie WaitForMultipleObjects aufrufen, verwenden Sie GetRequestHandle, um das Ereignishandle abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




