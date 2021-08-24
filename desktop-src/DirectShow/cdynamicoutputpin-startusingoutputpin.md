---
description: Die StartUsingOutputPin-Methode erhält Zugriff auf den Pin für einen Streamingvorgang.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: CDynamicOutputPin.StartUsingOutputPin-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4438c6670b0535711c453e64496ffd4b21263acab728e090024f9e1e01427969
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749450"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>CDynamicOutputPin.StartUsingOutputPin-Methode

Die `StartUsingOutputPin` -Methode erhält Zugriff auf den Pin für einen Streamingvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                           | Beschreibung                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                               |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>          | Unerwarteter Fehler.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ STATUS \_ GEÄNDERT**</dt> </dl> | Der Filter wurde beendet, oder die Stecknadel wurde geleert.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, bevor Sie Methoden aufrufen, die Daten an den verbundenen Eingabepin liefern oder den Medientyp der Verbindung ändern. Diese Regel gilt beispielsweise für die folgenden Methoden:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Rufen Sie anschließend die [**CDynamicOutputPin::StopUsingOutputPin-Methode**](cdynamicoutputpin-stopusingoutputpin.md) auf, um den Zugriff auf den Pin frei zu geben.

Wenn die Stecknadel blockiert ist, `StartUsingOutputPin` wartet darauf, dass die Blockierung des Pins aufgehoben wird. Wenn der Filter beendet wird, während die Methode wartet, gibt die Methode sofort VFW \_ E \_ STATE CHANGED \_ zurück. Der Pin behält die Anzahl der Aufrufe ohne einen entsprechenden Aufruf von `StartUsingOutputPin` **StopUsingOutputPin bei.** Wenn ein anderer Thread versucht, die Stecknadel zu blockieren, während diese Anzahl nicht 0 (null) ist, legt der Pin seinen Blockierungsstatus auf "Ausstehend" fest. Der Pin wird blockiert, sobald alle Streamingvorgänge abgeschlossen sind, im letzten Aufruf von **StopUsingOutputPin.**

Halten Sie den [**kritischen Abschnitt CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) nicht bei, wenn Sie diese Methode aufrufen. Andernfalls kann die Blockierung des Pins niemals aufgehoben werden, was zu einem Deadlock führt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




