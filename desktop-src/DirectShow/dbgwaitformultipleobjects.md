---
description: Wartet, bis ein (oder alle) der angegebenen Objekte signalisiert wird.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: DbgWaitForMultipleObjects-Funktion (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acab4a7f59fe0775e8e474f8a8a2342a5f29ae6266ee36432b0fc1b0e597141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654060"
---
# <a name="dbgwaitformultipleobjects-function"></a>DbgWaitForMultipleObjects-Funktion

Wartet, bis ein (oder alle) der angegebenen Objekte signalisiert wird.

In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Time out-Intervall abläuft, bevor die Objekte signalisiert werden. Rufen Sie zum Festlegen des Timeoutintervalls die [**DbgSetWaitTimeout-Funktion**](dbgsetwaittimeout.md) auf.

In einem Einzelhandels-Build entspricht diese Funktion der **WaitForMultipleObjects-Funktion** mit einem Time out-Intervall von INFINITE.

## <a name="syntax"></a>Syntax


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nCount* 
</dt> <dd>

Anzahl der Objekte.

</dd> <dt>

*lpHandles* 
</dt> <dd>

Array von Handles für Objekte der Größe *nCount*.

</dd> <dt>

*bWaitAll* 
</dt> <dd>

Boolescher Wert, der angibt, ob auf alle -Objekte gewartet werden soll. True **gibt** an, dass die Funktion darauf wartet, dass alle Objekte signalisiert werden. Andernfalls wird darauf gewartet, dass mindestens ein Objekt signalisiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Wartedebuggingfunktionen](wait-debugging-functions.md)
</dt> </dl>

 

 




