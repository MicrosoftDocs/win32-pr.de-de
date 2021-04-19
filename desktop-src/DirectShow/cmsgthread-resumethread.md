---
description: 'Verwendet die Microsoft Win32 ResumeThread-Funktion, um den Vorgang des Arbeitsthreads nach einem vorherigen aufrufsvorgang der cmsgthread:: SuspendThread-Member-Funktion fortzusetzen.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Cmsgthread. ResumeThread-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370836"
---
# <a name="cmsgthreadresumethread-method"></a>Cmsgthread. ResumeThread-Methode

Verwendet die Microsoft Win32 **ResumeThread** -Funktion, um den Vorgang des Arbeitsthreads nach einem vorherigen aufrufsvorgang der [**cmsgthread:: SuspendThread**](cmsgthread-suspendthread.md) -Member-Funktion fortzusetzen.

## <a name="syntax"></a>Syntax


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Member-Funktion erfolgreich ist, ist der Rückgabewert die vorherige anhalteanzahl des Threads. Wenn die Member-Funktion fehlschlägt, ist der Rückgabewert 0xFFFFFFFF. Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Win32 **GetLastError** -Funktion auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




