---
description: Die GetRequest-Methode wartet auf die nächste Anforderung.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: CABThread.GetRequest-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2527d43dfa59ab01bc57109bd2845e5da8286524612746067b1ff2f4cb2a3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103200"
---
# <a name="camthreadgetrequest-method"></a>CABThread.GetRequest-Methode

Die `GetRequest` -Methode wartet auf die nächste Anforderung.

## <a name="syntax"></a>Syntax


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.

## <a name="remarks"></a>Hinweise

Diese Methode wird blockiert, bis ein anderer Thread die [**METHODE CABThread::CallWorker**](camthread-callworker.md) aufruft. Anschließend wird der Parameter zurückgegeben, der an CallWorker übergeben wurde. Rufen Sie die [**METHODE TARThread::Reply**](camthread-reply.md) auf, um den anfordernden Thread freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




