---
description: 'Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit. Diese Methode überschreibt die ctransformfilter:: Receive-Methode.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Cvideotransformfilter. Receive-Methode (vtrans. h)
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
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367048"
---
# <a name="cvideotransformfilterreceive-method"></a>Cvideotransformfilter. Receive-Methode

Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit. Diese Methode überschreibt die [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode.

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

Diese Methode ruft [**cvideotransformfilter:: dendskipframe**](cvideotransformfilter-shouldskipframe.md) auf, um zu bestimmen, ob dieses Beispiel bereitgestellt oder einfach verworfen werden soll. Wenn " **dendskipframe** " **false** zurückgibt (was angibt, dass das Beispiel übermittelt werden soll), führt die Methode Folgendes aus:

1.  Ruft [**ctransformfilter:: initializeoutputsample**](ctransformfilter-initializeoutputsample.md) auf, um das Ausgabe Beispiel vorzubereiten
2.  Ruft [**ctransformfilter:: Transform**](ctransformfilter-transform.md) auf, um das Eingabe Beispiel zu verarbeiten. Diese Methode ist rein virtuell und muss in der abgeleiteten Klasse implementiert werden.
3.  Ruft [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md) auf, um das Ausgabe Beispiel bereitzustellen.

Außerdem prüft diese Methode, ob im Eingabe-oder Ausgabe Beispiel Formatänderungen durch Aufrufen von [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)durchgeführt werden. Wenn eine Formatänderung vorliegt, legt die-Methode den Verbindungstyp für die entsprechende PIN fest. Bevor der neue Typ festgelegt wird, wird **stopstreaming** aufgerufen. Nachdem der neue Typ festgelegt wurde, wird **startstreaming** aufgerufen. Diese Methoden können von der abgeleiteten Klasse zum Aktualisieren Ihres internen Zustands verwendet werden. Die abgeleitete Klasse muss möglicherweise auch das neue Format in der **Transformations** Methode überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




