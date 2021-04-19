---
description: Die Receive-Methode wird aufgerufen, wenn das Objekt ein Medien Beispiel aus der Ausgabe-PIN empfängt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Cpullpin. Receive-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361624"
---
# <a name="cpullpinreceive-method"></a>Cpullpin. Receive-Methode

Die- `Receive` Methode wird aufgerufen, wenn das-Objekt ein Medien Beispiel aus der Ausgabe-PIN empfängt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Mediums Sample.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Wenn Sie einen anderen Wert als S OK zurückgeben, \_ wird der datenzieh Thread beendet.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird immer dann aufgerufen, wenn ein neues Beispiel aus der Ausgabe-PIN eintrifft. Schreiben Sie diese Methode auf die gleiche Weise wie die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.

Die Zeitstempel im Beispiel geben die Byte Offsets relativ zur ursprünglichen Startposition an, die in der [**cpullpin:: Seek**](cpullpin-seek.md) -Methode angegeben wurde.

Die Startposition wird auf die nächste Ausrichtungs Grenze gerundet, und die Position des Stopps wird auf die nächste Ausrichtungs Grenze aufgerundet. Außerdem wird die Dauer verwendet, wenn die anhalteposition die Gesamtdauer überschreitet.

Alle Zeitstempel werden als Byte Offset multipliziert mit 10 Millionen angegeben, der als Konstante Einheiten definiert ist. Folglich ist eine Sekunde eine Sekunde ein Byte. Um die tatsächlichen Byte Offsets zu ermitteln, müssen Sie [**imediasample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) aufrufen und die Ergebnisse nach Einheiten aufteilen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




