---
description: 'CTransformInputPin.Receive-Methode: Die Receive-Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die IMemInputPin::Receive-Methode.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: CTransformInputPin.Receive-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51ae6614544cd7045689f674ce90e672e3bce4ea8ee36486775892f95a5385fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538545"
---
# <a name="ctransforminputpinreceive-method"></a>CTransformInputPin.Receive-Methode

Die `Receive` -Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die [**IMemInputPin::Receive-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

## <a name="syntax"></a>Syntax


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                             | Beschreibung                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin wird gerade geleert. Das Beispiel wurde abgelehnt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                        |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) des Pins auf, die den Streamingzustand des Pins überprüft und auf Formatänderungen im Medientyp überprüft. Anschließend wird die [**CTransformFilter::Receive-Methode**](ctransformfilter-receive.md) des Filters aufgerufen, die das Beispiel verarbeitet und nachgeschaltet liefert.

Wenn der Filter nach der Rückgabe dieser Methode auf das Beispiel zugreifen muss, sollte er einen Verweiszähler durch Aufrufen der **IUnknown::AddRef-Methode** für das Beispiel besitzen. Beispielsweise benötigen einige Decoderfilter das aktuelle Beispiel, um das nächste Beispiel zu decodieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




