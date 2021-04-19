---
description: 'Die EndOfStream-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis ein neuer Run-Befehl an den Filter ausgegeben wird. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Crenderedinputpin. EndOf Stream-Methode (amextra. h)
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
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373821"
---
# <a name="crenderedinputpinendofstream-method"></a>Crenderedinputpin. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden, bis ein neuer Run-Befehl an den Filter ausgegeben wird. Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlercode zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der Filter ausgeführt wird, sendet diese Methode ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Graph-Manager. Andernfalls wird von ein Flag festgelegt, sodass das EC \_ Complete-Ereignis gesendet wird, wenn der Filter das nächste Mal ausgeführt wird. Durch das Leeren des Filters wird das Flag gelöscht.

Sie sollten diese Methode überschreiben, um die streamingabsperre der PIN zu halten:


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



Wenn die Filterprozesse außerdem asynchron Aufrufe **empfangen** , sollte die PIN warten, bis das "EC Complete"-Ereignis gesendet wird, \_ bis der Filter alle ausstehenden Stichproben verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amextra. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Crenderedinputpin-Klasse**](crenderedinputpin.md)
</dt> </dl>

 

 




