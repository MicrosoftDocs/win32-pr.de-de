---
description: 'COutputQueue.COutputQueue-Konstruktor : Konstruktormethode.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: COutputQueue.COutputQueue-Konstruktor (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bf50314fd0ceb1afbe00c5a6a63708cc79ab38d77931c80b086039c7ca9704c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087240"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>COutputQueue.COutputQueue-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInputPin* 
</dt> <dd>

Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins. Das -Objekt liefert Beispiele an diesen Pin.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Rückgabecode.** Legen Sie den Wert auf S \_ OK fest, bevor Sie diese Methode aufrufen. Bei der Rückgabe *empfängt phr* einen Wert, der den Erfolg oder Fehler der Methode angibt.

</dd> <dt>

*bAuto* 
</dt> <dd>

Flag, das angibt, ob das Objekt entscheidet, wann eine Warteschlange erstellt werden soll. True **gibt an,** dass das -Objekt nur dann eine Warteschlange erstellt, wenn der Eingabepin blockiert werden kann. False **gibt** mit dem *Parameter bQueue* an, ob eine Warteschlange erstellt werden soll.

</dd> <dt>

*bQueue* 
</dt> <dd>

Wenn *bAuto* **true ist,** wird dieser Parameter ignoriert. Wenn *bAuto* **FALSE ist,** gibt dieses Flag an, ob eine Warteschlange erstellt werden soll.

</dd> <dt>

*lBatchSize* 
</dt> <dd>

Maximale Anzahl von Stichproben, die in einem Batch zu liefern sind.

</dd> <dt>

*bBatchExact* 
</dt> <dd>

Flag, das angibt, ob genaue Batchgrößen verwendet werden. True **gibt an,** dass das Objekt auf *lBatchSize-Stichproben* wartet, bevor sie an den Eingabepin zu liefern sind. False **gibt an,** dass das Objekt Stichproben liefert, während es sie empfängt.

</dd> <dt>

*lListSize* 
</dt> <dd>

Cachegröße für die Warteschlange. Der Standardwert DEFAULTCACHE ist eine Konstante, die für die [**CBaseList-Klasse definiert**](cbaselist.md) ist.

</dd> <dt>

*dwPriority* 
</dt> <dd>

Priorität des Threads, der Beispiele liefert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn *bAuto* **true ist,** ruft das Objekt die [**IMemInputPin::ReceiveCanBlock-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) auf dem Downstreampin auf. Wenn **ReceiveCanBlock** S OK zurückgibt (was bedeutet, dass die Pin bei \_ [**IMemInputPin::Receive-Aufrufen**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) blockiert werden kann), erstellt das Objekt einen Thread für die Bereitstellung von Beispielen. Andernfalls wird kein Thread erstellt.

Wenn *bAuto* **FALSE ist,** bestimmt der Wert *von bQueue,* ob ein Thread erstellt werden soll.

Wenn das -Objekt einen Thread erstellt, wird das Threadhandles der [**Membervariablen COutputQueue::m \_ hThread**](coutputqueue-m-hthread.md) zugewiesen. Die Threadprozedur [**ist COutputQueue::InitialThreadProc,**](coutputqueue-initialthreadproc.md)und der Threadparameter ist ein Zeiger darauf. Das -Objekt erstellt auch eine Warteschlange zum Enthalten von Stichproben, die von der [**Membervariablen COutputQueue::m \_ List**](coutputqueue-m-list.md) angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




