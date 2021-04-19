---
description: Die cqueue-Klassen Vorlage implementiert eine einfache, statisch formatierte Warteschlange.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Cqueue-Klasse (wxutil. h)
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
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359715"
---
# <a name="cqueue-class"></a>Cqueue-Klasse

Die **cqueue** -Klassen Vorlage implementiert eine einfache, statisch formatierte Warteschlange.



| Öffentliche Methoden                                  | BESCHREIBUNG                             |
|-------------------------------------------------|-----------------------------------------|
| [**Cqueue**](cqueue-cqueue.md)                 | Konstruktormethode.                     |
| [**~ Cqueue**](cqueue--cqueue.md)               | Dekonstruktormethode.                      |
| [**Getqueueobject**](cqueue-getqueueobject.md) | Ruft das nächste Element aus der Warteschlange ab. |
| [**Putqueueobject**](cqueue-putqueueobject.md) | Fügt ein Element in die Warteschlange ein.            |



 

## <a name="remarks"></a>Bemerkungen

Der Klassenkonstruktor gibt die Größe der Warteschlange an. Verwenden Sie das [**cqueue::P utqueueobject**](cqueue-putqueueobject.md) , um ein Element in die Warteschlange zu versetzen, und die [**cqueue:: getqueueobject**](cqueue-getqueueobject.md) -Methode, um ein Element aus der Warteschlange zu entfernen. Wenn die Warteschlange voll ist, wird die **putqueueobject** -Methode blockiert, bis ein Element aus der Warteschlange entfernt wird. Wenn die Warteschlange leer ist, wird **getqueueobject** blockiert, bis ein Element in die Warteschlange eingereiht wird. Der Template-Parameter gibt den Typ des Elements an. Beispiel:


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



Die-Klasse verwendet zwei Semaphor zum Steuern von Warteschlangen Vorgängen, eine "Get"-Semaphor und eine "Put"-Semaphor. Die [**getqueueobject**](cqueue-getqueueobject.md) -Methode wartet auf das "Get"-Semaphor (mit der **WaitForSingleObject** -Funktion) und gibt das "Put"-Semaphor frei (mit der **ReleaseSemaphore** -Funktion). Die [**putqueueobject**](cqueue-putqueueobject.md) -Methode wartet auf das "Put"-Semaphor und gibt das "Get"-Semaphor frei. Die-Klasse verwendet einen kritischen Abschnitt, um Warteschlangen Vorgänge zwischen mehreren Threads zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




