---
description: Die Receive-Methode empfängt ein Medienbeispiel, verarbeitet es und übergibt ein Ausgabebeispiel an den Downstreamfilter.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: CTransformFilter.Receive-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a0c57cf6826274169a5984dd794e1ba9a5b8e78c7ffb774b00b05f16384e4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953409"
---
# <a name="ctransformfilterreceive-method"></a>CTransformFilter.Receive-Methode

Die `Receive` -Methode empfängt ein Medienbeispiel, verarbeitet es und übergibt ein Ausgabebeispiel an den Downstreamfilter.

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

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) im Eingabebeispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                             | Beschreibung                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Upstreamfilter sollte das Senden von Beispielen beenden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                         |



 

## <a name="remarks"></a>Hinweise

Der Eingabepin des Filters ruft diese Methode auf, wenn er ein Beispiel empfängt. Diese Methode ruft die [**CTransformFilter::InitializeOutputSample-Methode**](ctransformfilter-initializeoutputsample.md) auf, die ein neues Ausgabebeispiel vorbereitet. Anschließend wird die [**CTransformFilter::Transform-Methode**](ctransformfilter-transform.md) aufgerufen, die von der abgeleiteten Klasse implementiert werden muss. Die **Transform-Methode** verarbeitet die Eingabedaten und erzeugt Ausgabedaten.

Wenn die **Transform-Methode** S \_ FALSE zurückgibt, `Receive` löscht die Methode dieses Beispiel. Im ersten gelöschten Beispiel sendet der Filter ein [**EC \_ QUALITY \_ CHANGE-Ereignis**](ec-quality-change.md) an den Filterdiagramm-Manager. Andernfalls liefert der Filter das Ausgabebeispiel, wenn die **Transform-Methode** S \_ OK zurückgibt. Dazu ruft sie die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) auf dem Nach-Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




