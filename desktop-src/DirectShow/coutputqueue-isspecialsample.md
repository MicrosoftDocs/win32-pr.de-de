---
description: Die isspecialsample-Methode bestimmt, ob Daten in der Warteschlange eine Kontroll Nachricht sind.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Coutputqueue. isspecialsample-Methode (outputq. h)
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
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358284"
---
# <a name="coutputqueueisspecialsample-method"></a>Coutputqueue. isspecialsample-Methode

Die- `IsSpecialSample` Methode bestimmt, ob Daten in der Warteschlange eine Kontroll Meldung sind.

## <a name="syntax"></a>Syntax


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf ein Element in der Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn *psample* eine Steuer Meldung ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die [**coutputqueue:: queuesample**](coutputqueue-queuesample.md) -Methode kann neben Medien Beispielen auch Steuerungs Meldungen empfangen. Eine Kontroll Meldung ist eine definierte Konstante (in einen langen \_ ptr-Typ umgewandelt), die den Thread anweist, eine Aktion auszuführen. Steuerungs Meldungen enthalten keine Mediendaten. Weitere Informationen finden Sie unter **coutputqueue:: queuesample**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




