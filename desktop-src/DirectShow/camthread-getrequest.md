---
description: Die GetRequest-Methode wartet auf die nächste Anforderung.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Camthread. GetRequest-Methode (wxutil. h)
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
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359645"
---
# <a name="camthreadgetrequest-method"></a>Camthread. GetRequest-Methode

Die- `GetRequest` Methode wartet auf die nächste Anforderung.

## <a name="syntax"></a>Syntax


```C++
DWORD GetRequest();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird blockiert, bis ein anderer Thread die Methode " [**camthread:: callworker**](camthread-callworker.md) " aufruft. Anschließend wird der an callworker übergebenen Parameter zurückgegeben. Ruft die Methode " [**camthread:: Reply**](camthread-reply.md) " auf, um den anfordernden Thread freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




