---
description: Die NotifyThread-Methode benachrichtigt den Thread, dass die Warteschlange Daten enthält.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: COutputQueue.NotifyThread-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d96fa39c912502234e7ff513badfd787032a41fd1f951b6d89f79194a6d4e72b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073724"
---
# <a name="coutputqueuenotifythread-method"></a>COutputQueue.NotifyThread-Methode

Die `NotifyThread` -Methode benachrichtigt den Thread, dass die Warteschlange Daten enthält.

## <a name="syntax"></a>Syntax


```C++
void NotifyThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Speichern Sie den kritischen Abschnitt, bevor Sie diese Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




