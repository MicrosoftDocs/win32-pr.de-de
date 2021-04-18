---
description: 'Die Thread proc-Methode ist die Thread Prozedur für den Arbeits Thread. Diese Methode implementiert die pure Virtual camthread:: ThreadProc-Methode.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Csourcestream. ThreadProc-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365962"
---
# <a name="csourcestreamthreadproc-method"></a>Csourcestream. ThreadProc-Methode

Die- `ThreadProc` Methode ist die Thread Prozedur für den Arbeits Thread. Diese Methode implementiert die pure Virtual [**camthread:: ThreadProc**](camthread-threadproc.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn der Thread erfolgreich abgeschlossen wurde, oder andernfalls 1. Wenn der Rückgabewert 1 ist, werden die Ressourcen des Threads möglicherweise trotzdem zugeordnet.

## <a name="remarks"></a>Bemerkungen

Diese Methode wartet unbegrenzt auf Thread Anforderungen, indem die Methode " [**camthread:: GetRequest**](camthread-getrequest.md) " aufgerufen wird. Wenn eine [**csourcestream:: Run**](csourcestream-run.md) -oder [**csourcestream::P ause**](csourcestream-pause.md) -Anforderung empfangen wird, wird die [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen. Die Methode **dobufferprocessingloop** überträgt Daten, bis Sie eine [**csourcestream:: Stoppanforderung**](csourcestream-stop.md) empfängt. Die Thread Prozedur wird beendet, wenn Sie eine [**csourcestream:: Exit**](csourcestream-exit.md) -Anforderung empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




