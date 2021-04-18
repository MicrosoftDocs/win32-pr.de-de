---
description: Die ThreadProc-Methode ist die Thread Prozedur.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Camthread. ThreadProc-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352035"
---
# <a name="camthreadthreadproc-method"></a>Camthread. ThreadProc-Methode

Die- `ThreadProc` Methode ist die Thread Prozedur.

## <a name="syntax"></a>Syntax


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, dessen Bedeutung durch die abgeleitete Klasse definiert wird.

## <a name="remarks"></a>Bemerkungen

Dies ist eine reine virtuelle Methode. Implementieren Sie diese Methode in der abgeleiteten Klasse, um eine Thread Prozedur bereitzustellen. Wenn die Methode " [**camthread:: Create**](camthread-create.md) " einen Thread erstellt, erhält Sie die Adresse der " [**camthread:: initialthleproc**](camthread-initialthreadproc.md) "-Methode, die wiederum ihre ThreadProc-Methode aufruft.

In der Regel wird von der ThreadProc-Methode eine Schleife eingegeben, die Anforderungen abruft (durch Aufrufen der Methoden [**camthread:: GetRequest**](camthread-getrequest.md) oder [**camthread:: CheckRequest**](camthread-checkrequest.md) ) und die Daten verarbeitet.

Wenn diese Methode zurückgegeben wird, wird der Thread beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




