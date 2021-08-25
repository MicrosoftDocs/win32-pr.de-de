---
description: 'COutputQueue.BeginFlush-Methode: Die BeginFlush-Methode startet einen Leerungsvorgang.'
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: COutputQueue.BeginFlush-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7b002c03ee0bfb95733ac9af0f6e88444cc6a42bec2af7d9a40a307d83d2fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909650"
---
# <a name="coutputqueuebeginflush-method"></a>COutputQueue.BeginFlush-Methode

Die `BeginFlush` -Methode startet einen Leerungsvorgang.

## <a name="syntax"></a>Syntax


```C++
void BeginFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode legt die [**COutputQueue::m \_ bFlushing-Membervariable**](coutputqueue-m-bflushing.md) auf **TRUE fest.** Wenn das Objekt einen Thread verwendet, ruft der Thread die [**COutputQueue::FreeSamples-Methode**](coutputqueue-freesamples.md) auf, um ausstehende Stichproben frei zu geben. Andernfalls ruft das -Objekt **FreeSamples während** der [**COutputQueue::EndFlush-Methode**](coutputqueue-endflush.md) auf. Diese Methode legt auch die [**COutputQueue::m hr-Membervariable \_**](coutputqueue-m-hr.md) auf S FALSE fest, wodurch das Objekt alle \_ neuen Stichproben verwirft.

Das -Objekt übergibt die Leerungsbenachrichtigung downstream, indem es die [**IPin::BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Eingabepin aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




