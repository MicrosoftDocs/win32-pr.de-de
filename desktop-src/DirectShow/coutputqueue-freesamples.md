---
description: Die FreeSamples-Methode gibt alle ausstehenden Beispiele frei.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: COutputQueue.FreeSamples-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2cc87047d6dc48494fc225b5a0b4c4ad7bcb69f0f7341580f8c48c1440470bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954159"
---
# <a name="coutputqueuefreesamples-method"></a>COutputQueue.FreeSamples-Methode

Die `FreeSamples` -Methode gibt alle ausstehenden Beispiele frei.

## <a name="syntax"></a>Syntax


```C++
void FreeSamples();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode entfernt alle ausstehenden Stichproben aus der Warteschlange und aus dem Beispielarray.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




