---
description: Die ReceiveCanBlock-Methode bestimmt, ob Aufrufe der IMemInputPin::Receive-Methode blockiert werden können. Diese Methode implementiert die IMemInputPin::ReceiveCanBlock-Methode.
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: CBaseInputPin.ReceiveCanBlock-Methode (Amfilter.h)
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
ms.openlocfilehash: 4ece7243c145d34ed06e29b2a29ae9847e682981337b96a47976c20eb76272d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823852"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>CBaseInputPin.ReceiveCanBlock-Methode

Die `ReceiveCanBlock` -Methode bestimmt, ob Aufrufe der [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) blockiert werden können. Diese Methode implementiert die [**IMemInputPin::ReceiveCanBlock-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock)

## <a name="syntax"></a>Syntax


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die Stecknadel wird bei einem Aufruf von **Receive** nicht blockiert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Stecknadel kann bei einem Aufruf von Receive blockiert **werden.**<br/>    |



 

## <a name="remarks"></a>Hinweise

Gibt S \_ FALSE zurück, wenn Aufrufe der **Receive-Methode** garantiert nicht blockiert werden. Andernfalls wird S \_ OK oder ein Fehlercode zurückgegeben. Wenn die **Receive-Methode** **Receive** für einen Downstreampin aufruft, wird der Downstreampin möglicherweise blockiert. `ReceiveCanBlock` muss diesen Faktor berücksichtigen.

Ein Upstreamfilter kann diese Methode verwenden, um seine Threadingstrategie zu bestimmen. Wenn die **Receive-Methode** blockiert werden kann, entscheidet sich der Upstreamfilter möglicherweise für die Verwendung eines Arbeitsthreads, der Daten puffert. Eine Implementierung dieser Strategie finden Sie in der [**COutputQueue-Klasse.**](coutputqueue.md)

In der Basisklasse gibt diese Methode S OK zurück, wenn eine der folgenden Punkte \_ zutrifft:

-   Der Filter verfügt über keine Ausgabepins.
-   Ein Eingabepin, der mit diesem Filter verbunden ist, signalisiert, dass er möglicherweise blockiert wird.
-   Ein Eingabepin, der mit diesem Filter verbunden ist, unterstützt die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




