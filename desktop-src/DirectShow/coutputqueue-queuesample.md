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
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910068"
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

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt dem Ende der Warteschlange ein Beispiel hinzu. Halten Sie den kritischen Abschnitt vor dem Aufrufen dieser Methode, und rufen Sie ihn nur auf, wenn das -Objekt einen Thread verwendet, um Beispiele zu liefern. Um zu bestimmen, ob das Objekt einen Thread verwendet, rufen Sie die [**COutputQueue::IsQueued-Methode**](coutputqueue-isqueued.md) auf.

Diese Methode kann auch verwendet werden, um Steuernachrichten in die Warteschlange zu stellen. Eine Steuermeldung ist eine definierte Konstante (in einen LONG PTR-Typ wandelt), die den Thread anweisen, \_ eine Aktion durchzuführen. Die **COutputQueue-Klasse** definiert die in der folgenden Tabelle gezeigten Steuerungsmeldungen.



| Bezeichnung | Wert |
|---------------|----------------------------------------|
| `Message`       | Aktion                                 |
| PAKET VOM \_ PAKET "EOS"   | Stellen Sie eine Benachrichtigung über das Ende des Datenstroms zu. |
| NEUES \_ SEGMENT  | Geben Sie ein neues Segment an.                 |
| PAKET \_ ZURÜCKSETZEN | Setzen Sie den Status der Warteschlange zurück.          |
| PAKET \_ SENDEN  | Senden Sie einen Teilbatch von Beispielen.       |



 

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

 

 




