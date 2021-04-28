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
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084968"
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



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**CBaseInputPin::Receive-Methode**](cbaseinputpin-receive.md) des Pins auf, die den Streamingzustand des Pins überprüft und auf Formatänderungen im Medientyp überprüft. Anschließend wird die [**CTransformFilter::Receive-Methode**](ctransformfilter-receive.md) des Filters aufgerufen, die das Beispiel verarbeitet und nachgeschaltet übergibt.

Wenn der Filter nach der Rückgabe dieser Methode auf das Beispiel zugreifen muss, sollte er einen Verweiszähler durch Aufrufen der **IUnknown::AddRef-Methode** für das Beispiel besitzen. Beispielsweise benötigen einige Decoderfilter das aktuelle Beispiel, um das nächste Beispiel zu decodieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (streams.h enthalten)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




