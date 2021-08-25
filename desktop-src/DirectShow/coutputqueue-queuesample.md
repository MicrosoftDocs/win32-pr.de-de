---
description: Die QueueSample-Methode reiht ein Beispiel in die Warteschlange ein.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: COutputQueue.QueueSample-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909590"
---
# <a name="coutputqueuequeuesample-method"></a>COutputQueue.QueueSample-Methode

Die `QueueSample` -Methode reiht ein Beispiel in die Warteschlange ein.

## <a name="syntax"></a>Syntax


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode fügt dem Ende der Warteschlange ein Beispiel hinzu. Halten Sie den kritischen Abschnitt vor dem Aufrufen dieser Methode bei, und rufen Sie ihn nur auf, wenn das Objekt einen Thread zum Übermitteln von Beispielen verwendet. Um zu bestimmen, ob das Objekt einen Thread verwendet, rufen Sie die [**COutputQueue::IsQueued-Methode**](coutputqueue-isqueued.md) auf.

Diese Methode kann auch verwendet werden, um Steuernachrichten in die Warteschlange zu stellen. Eine Steuernachricht ist eine definierte Konstante (umwandlung in einen LONG \_ PTR-Typ), die den Thread anweist, eine Aktion auszuführen. Die **COutputQueue-Klasse** definiert die in der folgenden Tabelle gezeigten Steuermeldungen.



| Bezeichnung | Wert |
|---------------|----------------------------------------|
| `Message`       | Aktion                                 |
| EOS \_ PACKET   | Übermitteln sie eine Benachrichtigung über das Ende des Streams. |
| NEUES \_ SEGMENT  | Stellen Sie ein neues Segment bereit.                 |
| PAKET \_ ZURÜCKSETZEN | Setzen Sie den Status der Warteschlange zurück.          |
| SEND \_ PACKET  | Senden sie einen Teilbatch von Beispielen.       |



 

Dies ist eine geschützte Methode, die von der **COutputQueue-Klasse** intern verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




