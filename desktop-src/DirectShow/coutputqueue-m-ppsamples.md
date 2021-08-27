---
description: Array von Beispielen der Größe COutputQueue::m \_ lBatchSize.
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: COutputQueue::m_ppSamples Member (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103150"
---
# <a name="coutputqueuem_ppsamples-member"></a>COutputQueue::m \_ ppSamples-Member

Array von Beispielen der Größe [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Syntax


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Hinweise

Der Arbeitsthread pullt Stichproben aus der Warteschlange und platziert sie in diesem Array. Das Array wird an die [**IMemInputPin::ReceiveMultiple-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) übergeben. Wenn das Objekt keinen Arbeitsthread verwendet, platziert das -Objekt Beispiele direkt in diesem Array. Die [**COutputQueue::m \_ List-Membervariable**](coutputqueue-m-list.md) enthält die Warteschlange.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




