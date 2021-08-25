---
description: Die ThreadProc-Methode ist die Threadprozedur für den Arbeitsthread. Diese Methode implementiert die rein virtuelleCAMThread::ThreadProc-Methode.
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: CSourceStream.ThreadProc-Methode (Source.h)
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
ms.openlocfilehash: 10ef0d29ab46ada118dc97c2d767b8377556086b949b6b9969cf5671b51e5359
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915270"
---
# <a name="csourcestreamthreadproc-method"></a>CSourceStream.ThreadProc-Methode

Die `ThreadProc` -Methode ist die Threadprozedur für den Arbeitsthread. Diese Methode implementiert die rein [**virtuelleCAMThread::ThreadProc-Methode.**](camthread-threadproc.md)

## <a name="syntax"></a>Syntax


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn der Thread erfolgreich abgeschlossen wurde, andernfalls 1. Wenn der Rückgabewert 1 ist, werden die Ressourcen des Threads möglicherweise weiterhin zugeordnet.

## <a name="remarks"></a>Hinweise

Diese Methode wartet unbegrenzt auf Threadanforderungen, indem sie die [**METHODECAMThread::GetRequest**](camthread-getrequest.md) aufruft. Wenn sie eine [**CSourceStream::Run-**](csourcestream-run.md) oder [**CSourceStream::P ause-Anforderung**](csourcestream-pause.md) empfängt, ruft sie die [**CSourceStream::D oBufferProcessingLoop-Methode**](csourcestream-dobufferprocessingloop.md) auf. Die **DoBufferProcessingLoop-Methode** über pusht Daten, bis sie eine [**CSourceStream::Stop-Anforderung**](csourcestream-stop.md) empfängt. Die Threadprozedur wird beendet, wenn sie eine [**CSourceStream::Exit-Anforderung**](csourcestream-exit.md) empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




