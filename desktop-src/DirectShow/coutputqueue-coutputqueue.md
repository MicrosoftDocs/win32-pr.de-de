---
description: Konstruktormethode.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Coutputqueue. coutputqueue-Konstruktor (outputq. h)
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
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361583"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>Coutputqueue. coutputqueue-Konstruktor

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

*pinputpin* 
</dt> <dd>

Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN. Das-Objekt stellt Beispiele für diese PIN bereit.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Rückgabecode. Legen Sie \_ vor dem Aufrufen dieser Methode den Wert auf S OK fest. Bei der Rückgabe erhält *PHR* einen Wert, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.

</dd> <dt>

*Bauto* 
</dt> <dd>

Flag, das angibt, ob das Objekt entscheidet, wann eine Warteschlange erstellt werden soll. **True** gibt an, dass das Objekt nur dann eine Warteschlange erstellt, wenn die Eingabe-PIN blockiert werden kann. Wenn **false**, gibt der *bqueue* -Parameter an, ob eine Warteschlange erstellt werden soll.

</dd> <dt>

*bqueue* 
</dt> <dd>

Wenn *Bauto* **true** ist, wird dieser Parameter ignoriert. Wenn *Bauto* auf **false** festgelegt ist, gibt dieses Flag an, ob eine Warteschlange erstellt werden soll.

</dd> <dt>

*lbatchsize* 
</dt> <dd>

Maximale Anzahl von Samplings, die in einem Batch geliefert werden sollen.

</dd> <dt>

*bbatchexact* 
</dt> <dd>

Flag, das angibt, ob genaue Batch Größen verwendet werden sollen. **True** gibt an, dass das Objekt vor der Übermittlung an die eingabepin auf *lbatchsize* -Beispiele wartet. **False** gibt an, dass das-Objekt beim Empfang von Beispielen Beispiele liefert.

</dd> <dt>

*llistsize* 
</dt> <dd>

Cache Größe für die Warteschlange. Der Standardwert, defaultcache, ist eine Konstante, die für die [**cbaselist**](cbaselist.md) -Klasse definiert ist.

</dd> <dt>

*dwPriority* 
</dt> <dd>

Priorität des Threads, der Beispiele liefert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn " *Bauto* " den Wert " **true**" hat, ruft das Objekt die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode für die downstreampin auf. Wenn **receivecanblock** S OK zurückgibt \_ (was bedeutet, dass die PIN bei [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -aufrufen blockieren kann), erstellt das Objekt einen Thread zum Bereitstellung von Beispielen. Andernfalls wird kein Thread erstellt.

Wenn *Bauto* auf **false** festgelegt ist, bestimmt der Wert von *bqueue* , ob ein Thread erstellt wird.

Wenn das Objekt einen Thread erstellt, wird das Thread Handle der [**coutputqueue:: m \_ hThread**](coutputqueue-m-hthread.md) -Element Variablen zugewiesen. Die Thread Prozedur ist [**coutputqueue:: initialthread proc**](coutputqueue-initialthreadproc.md), und der Thread Parameter ist ein Zeiger auf dieses. Das-Objekt erstellt außerdem eine Warteschlange für die Aufnahme von Beispielen, die von der [**coutputqueue:: m \_ List**](coutputqueue-m-list.md) -Element Variable angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




