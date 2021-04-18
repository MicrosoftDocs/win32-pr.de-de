---
description: Verwendet die Microsoft Win32 SuspendThread-Funktion, um den Betrieb eines laufenden Threads anzuhalten.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Cmsgthread. SuspendThread-Methode (msgthrd. h)
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
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358793"
---
# <a name="cmsgthreadsuspendthread-method"></a>Cmsgthread. SuspendThread-Methode

Verwendet die Microsoft Win32 **SuspendThread** -Funktion, um den Betrieb eines laufenden Threads anzuhalten.

## <a name="syntax"></a>Syntax


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Member-Funktion erfolgreich ist, ist der Rückgabewert die vorherige anhalteanzahl des Threads. Wenn die Member-Funktion fehlschlägt, ist der Rückgabewert 0xFFFFFFFF. Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Win32 **GetLastError** -Funktion auf.

## <a name="remarks"></a>Bemerkungen

Der Client Thread ruft diese Member-Funktion auf, um den Betrieb des Arbeitsthreads anzuhalten. Der Arbeits Thread bleibt angehalten und wird erst ausgeführt, wenn ein zusätzlicher Befehl an die [**cmsgthread:: ResumeThread**](cmsgthread-resumethread.md) -Member-Funktion erfolgt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




