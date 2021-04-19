---
description: Verwendet die Microsoft Win32-Funktion getthreadpriority, um die Priorität des aktuellen Arbeitsthreads abzurufen.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Cmsgthread. getthreadpriority-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372281"
---
# <a name="cmsgthreadgetthreadpriority-method"></a>Cmsgthread. getthreadpriority-Methode

Verwendet die Microsoft Win32-Funktion **getthreadpriority** , um die Priorität des aktuellen Arbeitsthreads abzurufen.

## <a name="syntax"></a>Syntax


```C++
int GetThreadPriority();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Thread Priorität als Ganzzahl zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




