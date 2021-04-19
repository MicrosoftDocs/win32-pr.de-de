---
description: 'Die receivecanblock-Methode bestimmt, ob Aufrufe der IMemInputPin:: Receive-Methode blockiert werden könnten. Diese Methode implementiert die IMemInputPin:: receivecanblock-Methode.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Cbaseinputpin. receivecanblock-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369274"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>Cbaseinputpin. receivecanblock-Methode

Die- `ReceiveCanBlock` Methode bestimmt, ob Aufrufe der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode blockiert werden könnten. Diese Methode implementiert die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die PIN wird bei einem empfangenden **Empfang** nicht blockiert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die PIN kann bei einem **Empfangs Empfang** blockiert werden.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Gibt false zurück, \_ Wenn der Aufruf der **Receive** -Methode garantiert nicht blockiert wird. Andernfalls wird S \_ OK oder ein Fehlercode zurückgegeben. Wenn die **Receive** -Methode **Receive** -Befehle für eine nachgeschaltete Pin aufruft, kann die downstreampin blockiert werden. `ReceiveCanBlock` muss diesen Faktor berücksichtigen.

Mit dieser Methode kann ein upstreamfilter die Threading Strategie bestimmen. Wenn die **Receive** -Methode blockiert werden kann, kann der upstreamfilter entscheiden, einen Arbeits Thread zu verwenden, der Daten puffert. Eine Implementierung dieser Strategie finden Sie unter der [**coutputqueue**](coutputqueue.md) -Klasse.

In der Basisklasse gibt diese Methode S OK zurück, \_ Wenn einer der folgenden Punkte zutrifft:

-   Der Filter hat keine Ausgabe Pins.
-   Eine mit diesem Filter verbundene Eingabe-PIN signalisiert, dass Sie blockiert werden kann.
-   Die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle wird von einer mit diesem Filter verbundenen Eingabe-PIN nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




