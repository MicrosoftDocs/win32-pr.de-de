---
description: Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: Ctransformfilter. Receive-Methode (Transfrm. h)
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
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354709"
---
# <a name="ctransformfilterreceive-method"></a>Ctransformfilter. Receive-Methode

Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.

## <a name="syntax"></a>Syntax


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle für das Eingabe Beispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                             | Beschreibung                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Der upstreamfilter sollte das Senden von Beispielen abbrechen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                         |



 

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie ein Beispiel empfängt. Diese Methode ruft die [**ctransformfilter:: initializeoutputsample**](ctransformfilter-initializeoutputsample.md) -Methode auf, die ein neues Ausgabe Beispiel vorbereitet. Anschließend wird die [**ctransformfilter:: Transform**](ctransformfilter-transform.md) -Methode aufgerufen, die von der abgeleiteten Klasse implementiert werden muss. Die **Transformations** Methode verarbeitet die Eingabedaten und erzeugt Ausgabedaten.

Wenn die **Transformations** Methode S false zurückgibt \_ , `Receive` Löscht die Methode dieses Beispiel. Im ersten gelöschten Beispiel sendet der Filter ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager. Andernfalls liefert der  \_ Filter das Ausgabe Beispiel, wenn die Transform-Methode "S OK" zurückgibt. Zu diesem Zweck wird die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die downstreameingabepin aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




