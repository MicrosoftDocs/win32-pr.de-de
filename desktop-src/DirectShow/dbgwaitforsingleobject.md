---
description: Wartet, bis ein Objekt signalisiert wird.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: DbgWaitForSingleObject-Funktion (Wxdebug.h)
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
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749350"
---
# <a name="dbgwaitforsingleobject-function"></a>DbgWaitForSingleObject-Funktion

Wartet, bis ein Objekt signalisiert wird.

In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Time out-Intervall abläuft, bevor das Objekt signalisiert wird. Um das Timeoutintervall festzulegen, rufen Sie die [**DbgSetWaitTimeout-Funktion**](dbgsetwaittimeout.md) auf.

In einem Verkaufsbuild entspricht diese Funktion der **WaitForSingleObject-Funktion** mit einem Time out-Intervall von INFINITE.

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

Handle für das -Objekt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Wartedebuggen von Funktionen](wait-debugging-functions.md)
</dt> </dl>

 

 




