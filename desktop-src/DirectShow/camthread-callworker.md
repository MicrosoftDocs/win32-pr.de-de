---
description: Die CallWorker-Methode signalisiert dem Thread eine Anforderung.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: CABThread.CallWorker-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7ffee6a55191f8f41d7121f3801a4a6392f9869803ded40ed891817146828f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955399"
---
# <a name="camthreadcallworker-method"></a>CABThread.CallWorker-Methode

Die `CallWorker` -Methode signalisiert dem Thread eine Anforderung.

## <a name="syntax"></a>Syntax


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwParam* 
</dt> <dd>

Anforderungsparameter. Die abgeleitete Klasse definiert die Bedeutung des Parameters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.

## <a name="remarks"></a>Hinweise

Die [**METHODEN TGThread::GetRequest**](camthread-getrequest.md) und [**TGThread::CheckRequest**](camthread-checkrequest.md) rufen den Wert des *dwParam-Parameters* ab. Die GetRequest-Methode wird blockiert, bis `CallWorker` aufgerufen wird.

Diese Methode wird blockiert, bis die [**METHODE CABThread::Reply**](camthread-reply.md) aufgerufen wird. Der Rückgabewert ist der Parameter, der reply übergeben wird.

Diese Methode enthält die [**LOCKThread::m \_ AccessLock-Sperre**](camthread-m-accesslock.md) zum Serialisieren von Anforderungen. Rufen Sie daher diese Methode aus dem Thread selbst oder aus einer beliebigen Memberfunktion auf, die im Kontext des Threads ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




