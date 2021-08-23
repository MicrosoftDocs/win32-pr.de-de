---
description: Die CQueue-Klassenvorlage implementiert eine einfache Warteschlange mit statischer Größe.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: CQueue-Klasse (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c6225a393f8f6ff1848acc66c68b6d260b0c839f2cc9f1e24d06a11e88219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953979"
---
# <a name="cqueue-class"></a>CQueue-Klasse

Die **CQueue-Klassenvorlage** implementiert eine einfache Warteschlange mit statischer Größe.



| Öffentliche Methoden                                  | BESCHREIBUNG                             |
|-------------------------------------------------|-----------------------------------------|
| [**CQueue**](cqueue-cqueue.md)                 | Konstruktormethode.                     |
| [**~CQueue**](cqueue--cqueue.md)               | Destruktormethode.                      |
| [**GetQueueObject**](cqueue-getqueueobject.md) | Ruft das nächste Element aus der Warteschlange ab. |
| [**PutQueueObject**](cqueue-putqueueobject.md) | Versetzt ein Element in die Warteschlange.            |



 

## <a name="remarks"></a>Hinweise

Der Klassenkonstruktor gibt die Größe der Warteschlange an. Verwenden Sie [**CQueue::P utQueueObject,**](cqueue-putqueueobject.md) um ein Element in die Warteschlange zu setzen, und die [**CQueue::GetQueueObject-Methode,**](cqueue-getqueueobject.md) um ein Element aus der Warteschlange zu entfernen. Wenn die Warteschlange voll ist, wird die **PutQueueObject-Methode** blockiert, bis ein Element aus der Warteschlange entfernt wird. Wenn die Warteschlange leer ist, wird **das GetQueueObject** blockiert, bis ein Element in die Warteschlange gestellt wird. Der Vorlagenparameter gibt den Typ des Elements an. Beispiel:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



Die -Klasse verwendet zwei Semaphore, um Warteschlangenvorgänge zu steuern, ein "get"-Semaphor und ein "put"-Semaphor. Die [**GetQueueObject-Methode**](cqueue-getqueueobject.md) wartet auf das "get"-Semaphor (mithilfe der **WaitForSingleObject-Funktion)** und gibt das "put"-Semaphor frei (mithilfe der **ReleaseSemaphore-Funktion).** Die [**PutQueueObject-Methode**](cqueue-putqueueobject.md) wartet auf das "put"-Semaphor und gibt das "get"-Semaphor frei. Die -Klasse verwendet einen kritischen Abschnitt, um Warteschlangenvorgänge zwischen mehreren Threads zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




