---
description: Verwendet die Microsoft Win32 SuspendThread-Funktion, um den Vorgang eines ausgeführten Threads an angehalten.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: CMsgThread.SuspendThread-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5242c8708c07beb85d297dff706dbe192f59f1f7b46b05eba7362c9f0182d52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915740"
---
# <a name="cmsgthreadsuspendthread-method"></a>CMsgThread.SuspendThread-Methode

Verwendet die Microsoft Win32 **SuspendThread-Funktion,** um den Vorgang eines ausgeführten Threads an angehalten.

## <a name="syntax"></a>Syntax


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Memberfunktion erfolgreich ausgeführt wird, ist der Rückgabewert die vorherige Suspendanzahl des Threads. Wenn die Memberfunktion fehlschlägt, wird der Rückgabewert 0xFFFFFFFF. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie die Microsoft Win32 **GetLastError-Funktion** auf.

## <a name="remarks"></a>Hinweise

Der Clientthread ruft diese Memberfunktion auf, um den Vorgang des Arbeitsthreads an angehalten. Der Arbeitsthread bleibt angehalten und wird erst ausgeführt, wenn ein zusätzlicher Aufruf der [**CMsgThread::ResumeThread-Memberfunktion**](cmsgthread-resumethread.md) erfolgt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




