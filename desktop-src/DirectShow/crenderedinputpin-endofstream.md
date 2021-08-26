---
description: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden, bis ein neuer Ausführungsbefehl für den Filter ausgegeben wird. Diese Methode implementiert die IPin::EndOfStream-Methode.
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: CRenderedInputPin.EndOfStream-Methode (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26f7a5075e06a3943978a8e938f034fbabcaddfa31c9ffa2a2b37d33a0120640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107990"
---
# <a name="crenderedinputpinendofstream-method"></a>CRenderedInputPin.EndOfStream-Methode

Die -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden, bis ein neuer `EndOfStream` Ausführungsbefehl für den Filter ausgegeben wird. Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, andernfalls ein Fehlercode.

## <a name="remarks"></a>Hinweise

Wenn der Filter ausgeführt wird, sendet diese Methode ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) an den Filter Graph Manager. Andernfalls legt ein Flag fest, sodass das EC \_ COMPLETE-Ereignis gesendet wird, wenn der Filter das nächste Mal ausgeführt wird. Durch Leeren des Filters wird das Flag geleert.

Sie sollten diese Methode überschreiben, um die Streamingsperre des Pins zu halten:


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



Wenn der Filter  Receive-Aufrufe asynchron verarbeitet, sollte der Pin außerdem warten, bis das EC COMPLETE-Ereignis gesendet wird, bis der Filter alle ausstehenden \_ Stichproben verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CRenderedInputPin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




