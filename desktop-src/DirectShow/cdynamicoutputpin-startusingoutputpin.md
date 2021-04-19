---
description: Die startusingoutputpin-Methode erhält Zugriff auf die PIN für einen Streamingvorgang.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Cdynamicoutputpin. startusingoutputpin-Methode (amfilter. h)
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
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359772"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>Cdynamicoutputpin. startusingoutputpin-Methode

Die `StartUsingOutputPin` Methode erhält Zugriff auf die PIN für einen Streamingvorgang.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                           | Beschreibung                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                               |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>          | Unerwarteter Fehler.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ Status \_ geändert**</dt> </dl> | Der Filter wurde beendet, oder die PIN wurde mit dem leeren begonnen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Methode auf, bevor Sie Methoden aufrufen, die Daten an die verbundene Eingabe-PIN übermitteln oder den Medientyp der Verbindung ändern. Diese Regel gilt z. b. für die folgenden Methoden:

-   [**Cdynamicoutputpin:: changeoutputformat**](cdynamicoutputpin-changeoutputformat.md)
-   [**Cdynamicoutputpin:: changemediatype**](cdynamicoutputpin-changemediatype.md)
-   [**Cdynamicoutputpin::D ynamikreconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**Cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md)
-   [**Cbaseoutputpin::D eliverendof Stream**](cbaseoutputpin-deliverendofstream.md)
-   [**Cbaseoutputpin::D elivernewsegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Anschließend können Sie die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode aufrufen, um den Zugriff auf die PIN freizugeben.

Wenn die PIN blockiert ist, `StartUsingOutputPin` wartet darauf, dass die Blockierung der PIN aufgehoben wird. Wenn der Filter während der Wartezeit der Methode angehalten wird, gibt die Methode sofort VFW \_ E \_ State \_ Changed zurück. Die PIN behält, wie oft `StartUsingOutputPin` ohne einen entsprechenden Aufruf von **stopusingoutputpin** aufgerufen wurde. Wenn ein anderer Thread versucht, die PIN zu blockieren, während diese Anzahl ungleich NULL ist, legt die PIN ihren Blockierungs Status auf "Ausstehend" fest. Die PIN wird blockiert, sobald alle Streamingvorgänge abgeschlossen sind, und zwar im letzten Rückruf von **stopusingoutputpin**.

Wenn Sie diese Methode aufrufen, dürfen Sie nicht den Abschnitt " [**cdynamicoutputpin:: m \_ blockstatuelock**](cdynamicoutputpin-m-blockstatelock.md) Critical" speichern. Andernfalls kann, wenn die PIN blockiert ist, nie die Blockierung aufgehoben werden, was zu einem Deadlock führt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




