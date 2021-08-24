---
description: Die SendAnyway-Methode stellt alle ausstehenden Beispiele bereit.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: COutputQueue.SendAnyway-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4aed3cdd37c50f20b48922c8c711266a111680506813ab4572800abbca971343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831760"
---
# <a name="coutputqueuesendanyway-method"></a>COutputQueue.SendAnyway-Methode

Die `SendAnyway` -Methode stellt alle ausstehenden Beispiele bereit.

## <a name="syntax"></a>Syntax


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die [**COutputQueue::m \_ bBatchExact-Membervariable**](coutputqueue-m-bbatchexact.md) **TRUE** ist, füllt das -Objekt das [**COutputQueue::m \_ ppSamples-Array**](coutputqueue-m-ppsamples.md) aus, bevor ein Batch von Stichproben übermittelt wird. Rufen Sie diese Methode auf, um einen Teilbatch zu übermitteln. Beispielsweise ruft die [**COutputQueue::EOS-Methode**](coutputqueue-eos.md) `SendAnyway` auf, um End-of-Stream-Nachrichten zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




