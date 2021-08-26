---
description: Die Receive-Methode empfängt ein Medienbeispiel, verarbeitet es und übermittelt ein Ausgabebeispiel an den Downstreamfilter. Diese Methode überschreibt die CTransformFilter::Receive-Methode.
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: CVideoTransformFilter.Receive-Methode (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bce69d5f14a522f403eed54b56a340ab02316507766c0cc6d60ff897ec73541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998510"
---
# <a name="cvideotransformfilterreceive-method"></a>CVideoTransformFilter.Receive-Methode

Die `Receive` -Methode empfängt ein Medienbeispiel, verarbeitet es und übermittelt ein Ausgabebeispiel an den Downstreamfilter. Diese Methode überschreibt die [**CTransformFilter::Receive-Methode.**](ctransformfilter-receive.md)

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

Diese Methode ruft [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) auf, um zu bestimmen, ob dieses Beispiel übermittelt oder einfach verworfen werden soll. Wenn **ShouldSkipFrame** **FALSE** zurückgibt (was angibt, dass das Beispiel übermittelt werden soll), führt die Methode folgende Schritte aus:

1.  Ruft [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) auf, um das Ausgabebeispiel vorzubereiten.
2.  Ruft [**CTransformFilter::Transform**](ctransformfilter-transform.md) auf, um das Eingabebeispiel zu verarbeiten. Diese Methode ist rein virtuell und muss in der abgeleiteten Klasse implementiert werden.
3.  Ruft [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) auf, um das Ausgabebeispiel zu übermitteln.

Außerdem überprüft diese Methode auf Formatänderungen im Eingabe- oder Ausgabebeispiel, indem [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)aufgerufen wird. Wenn eine Formatänderung erfolgt, legt die -Methode den Verbindungstyp auf dem entsprechenden Pin fest. Bevor der neue Typ festgelegt wird, ruft er **StopStreaming auf.** Nachdem der neue Typ festgelegt wurde, ruft er **StartStreaming auf.** Die abgeleitete Klasse kann diese Methoden verwenden, um ihren internen Zustand zu aktualisieren. Die abgeleitete Klasse muss möglicherweise auch in ihrer **Transform-Methode** nach dem neuen Format suchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




