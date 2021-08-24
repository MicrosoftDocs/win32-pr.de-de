---
description: Die Receive-Methode wird aufgerufen, wenn das -Objekt ein Medienbeispiel vom Ausgabepin empfängt. Die abgeleitete Klasse muss diese Methode implementieren.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: CPullPin.Receive-Methode (Pullpin.h)
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
ms.openlocfilehash: fdf38c9c873dd8d95ae60341fc2f7dba02abff1f8b34fd89d0d1f720dc59b55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831540"
---
# <a name="cpullpinreceive-method"></a>CPullPin.Receive-Methode

Die `Receive` -Methode wird aufgerufen, wenn das -Objekt ein Medienbeispiel vom Ausgabepin empfängt. Die abgeleitete Klasse muss diese Methode implementieren.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Medienbeispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Wenn Sie einen anderen Wert als S \_ OK zurückgeben, wird der Daten-Pullthread nicht mehr angezeigt.

## <a name="remarks"></a>Hinweise

Diese Methode wird immer dann aufgerufen, wenn ein neues Beispiel vom Ausgabepin eintrifft. Schreiben Sie diese Methode auf die gleiche Weise wie die [**IMemInputPin::Receive-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

Die Zeitstempel im Beispiel geben die Byteoffsets relativ zur ursprünglichen Startposition an, die in der [**CPullPin::Seek-Methode angegeben**](cpullpin-seek.md) wurde.

Die Startposition wird auf die nächste Ausrichtungsgrenze abgerundet, und die Stoppposition wird auf die nächste Ausrichtungsgrenze aufgerundet. Wenn die Stoppposition die Gesamtdauer überschreitet, wird stattdessen die Dauer verwendet.

Alle Zeitstempel werden als Byteoffset multipliziert mit 10.000.000 angegeben, definiert als konstante EINHEITEN. Daher ist eine Sekunde ein Byte. Um die tatsächlichen Byteoffsets zu finden, rufen [**Sie IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) auf, und dividieren Sie die Ergebnisse durch UNITS.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPullPin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




