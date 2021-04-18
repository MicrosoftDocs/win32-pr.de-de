---
description: Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Dbgwaitformultipleobjects-Funktion (wxdebug. h)
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
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364539"
---
# <a name="dbgwaitformultipleobjects-function"></a>Dbgwaitformultipleobjects-Funktion

Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden.

In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Timeout Intervall abläuft, bevor die Objekte signalisiert werden. Um das Timeout Intervall festzulegen, müssen Sie die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion aufrufen.

In einem Einzelhandels Build entspricht diese Funktion der **WaitForMultipleObjects** -Funktion mit einem Timeout Intervall von unendlich.

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

Anzahl von Objekten.

</dd> <dt>

*lphandles* 
</dt> <dd>

Array von Handles zu Objekten, Größe *nCount*.

</dd> <dt>

*bwaitall* 
</dt> <dd>

Boolescher Wert, der angibt, ob auf alle-Objekte gewartet werden soll. **True** gibt an, dass die Funktion darauf wartet, dass alle Objekte signalisiert werden. Andernfalls wartet es darauf, dass mindestens ein Objekt signalisiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Wait-Debugging-Funktionen](wait-debugging-functions.md)
</dt> </dl>

 

 




