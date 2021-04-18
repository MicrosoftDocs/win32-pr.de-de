---
description: Die Queue Sample-Methode fügt ein Beispiel in die Warteschlange ein.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Coutputqueue. Queue Sample-Methode (outputq. h)
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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352835"
---
# <a name="coutputqueuequeuesample-method"></a>Coutputqueue. queuesample-Methode

Die- `QueueSample` Methode fügt ein Beispiel in die Warteschlange

## <a name="syntax"></a>Syntax


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt dem Ende der Warteschlange ein Beispiel hinzu. Halten Sie den kritischen Abschnitt vor dem Aufruf dieser Methode ein, und rufen Sie ihn nur auf, wenn das Objekt einen Thread zum Übermitteln von Beispielen verwendet. Um zu ermitteln, ob das Objekt einen Thread verwendet, nennen Sie die [**coutputqueue:: IsQueued**](coutputqueue-isqueued.md) -Methode.

Diese Methode kann auch verwendet werden, um Steuerungs Meldungen in der Warteschlange zu platzieren. Eine Kontroll Meldung ist eine definierte Konstante (in einen langen \_ ptr-Typ umgewandelt), die den Thread anweist, eine Aktion auszuführen. Die **coutputqueue** -Klasse definiert die in der folgenden Tabelle gezeigten Steuer Meldungen.



|               |                                        |
|---------------|----------------------------------------|
| `Message`       | Aktion                                 |
| EOS- \_ Paket   | Übermitteln Sie eine Benachrichtigung zum Ende des Datenstroms. |
| neues \_ Segment  | Übermitteln Sie ein neues Segment.                 |
| Paket zurücksetzen \_ | Setzt den Status der Warteschlange zurück.          |
| \_Paket senden  | Senden eines partiellen Batches von Beispielen.       |



 

Dabei handelt es sich um eine geschützte Methode, die von der **coutputqueue** -Klasse intern verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




