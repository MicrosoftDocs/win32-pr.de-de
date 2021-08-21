---
description: Die ThreadProc-Methode ruft Stichproben aus der Warteschlange ab und übergibt sie an den Eingabepin.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: COutputQueue.ThreadProc-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d37158d71a74726e9bf27e76ffedb076f99b7380ffcca4edfa95928767eedbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073634"
---
# <a name="coutputqueuethreadproc-method"></a>COutputQueue.ThreadProc-Methode

Die `ThreadProc` -Methode ruft Stichproben aus der Warteschlange ab und übergibt sie an den Eingabepin.

## <a name="syntax"></a>Syntax


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die [**COutputQueue::InitialThreadProc-Methode**](coutputqueue-initialthreadproc.md) ruft diese Methode auf, die die Hauptthreadschleife implementiert. Innerhalb der -Schleife führt die -Methode die folgenden Schritte aus:

1.  Ruft ein Beispiel für die Warteschlange ab.
2.  Wenn das Beispiel eine Steuermeldung ist, führt der Thread die Steuerelementaktion aus. Andernfalls wird das Beispiel in das [**Array COutputQueue::m \_ ppSamples**](coutputqueue-m-ppsamples.md) platziert.
3.  Wenn das Array voll ist (oder [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) **FALSE** ist), ruft der Thread die [**IMemInputPin::ReceiveMultiple-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) auf, um die Beispiele zu liefern.
4.  Wenn keine Stichproben in die Warteschlange gestellt werden, wartet der Thread auf das [**COutputQueue::m \_ hSem-Semaphor.**](coutputqueue-m-hsem.md)

Der Thread wird beendet, wenn die [**COutputQueue::m \_ bTerminate-Membervariable**](coutputqueue-m-bterminate.md) TRUE **wird.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




