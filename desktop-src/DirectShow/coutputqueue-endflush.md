---
description: 'COutputQueue.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: COutputQueue.EndFlush-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099008"
---
# <a name="coutputqueueendflush-method"></a>COutputQueue.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang.

## <a name="syntax"></a>Syntax


```C++
void EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das Objekt einen Thread verwendet, wartet diese Methode auf das [**Ereignis COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md) Der Thread signalisiert dieses Ereignis, nachdem alle ausstehenden Stichproben frei gegeben wurden. Wenn das Objekt keinen Thread verwendet, ruft diese Methode die [**COutputQueue::FreeSamples-Methode**](coutputqueue-freesamples.md) auf. Anschließend ruft die `EndFlush` -Methode die [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) auf dem Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




