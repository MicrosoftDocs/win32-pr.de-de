---
description: Wartet darauf, dass ein Objekt signalisiert wird.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Dbgwaitforsingleobject-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364478"
---
# <a name="dbgwaitforsingleobject-function"></a>Dbgwaitforsingleobject-Funktion

Wartet darauf, dass ein Objekt signalisiert wird.

In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Timeout Intervall abläuft, bevor das Objekt signalisiert wird. Um das Timeout Intervall festzulegen, müssen Sie die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion aufrufen.

In einem Einzelhandels Build entspricht diese Funktion der **WaitForSingleObject** -Funktion mit einem Timeout Intervall von unendlich.

## <a name="syntax"></a>Syntax


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*h* 
</dt> <dd>

Handle für das-Objekt.

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

 

 




