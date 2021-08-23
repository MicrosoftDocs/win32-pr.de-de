---
description: Die IsSpecialSample-Methode bestimmt, ob Daten in der Warteschlange eine Steuernachricht sind.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: COutputQueue.IsSpecialSample-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c192196869f86e8d78da2f6b38a661373e115753d99e554f4b7a868eb0b484fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688220"
---
# <a name="coutputqueueisspecialsample-method"></a>COutputQueue.IsSpecialSample-Methode

Die `IsSpecialSample` -Methode bestimmt, ob Daten in der Warteschlange eine Steuernachricht sind.

## <a name="syntax"></a>Syntax


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf ein Element in der Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** *wenn pSample* eine Steuermeldung ist, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die [**COutputQueue::QueueSample-Methode**](coutputqueue-queuesample.md) kann zusätzlich zu Medienbeispielen Steuermeldungen empfangen. Eine Steuermeldung ist eine definierte Konstante (in einen LONG PTR-Typ wandelt), die den Thread anweisen, \_ eine Aktion durchzuführen. Steuermeldungen enthalten keine Mediendaten. Weitere Informationen finden Sie unter **COutputQueue::QueueSample**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




