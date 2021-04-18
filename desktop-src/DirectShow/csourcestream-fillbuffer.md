---
description: Die FillBuffer-Methode füllt ein Medien Beispiel mit Daten.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Csourcestream. FillBuffer-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371061"
---
# <a name="csourcestreamfillbuffer-method"></a>Csourcestream. FillBuffer-Methode

Die- `FillBuffer` Methode füllt ein Medien Beispiel mit Daten.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Ende des Streams<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss von der abgeleiteten Klasse implementiert werden.

Das für diese Methode angegebene Medien Beispiel hat keine Zeitstempel. Die abgeleitete Klasse sollte die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode aufrufen, um die Zeitstempel festzulegen. Wenn dies für den Medientyp angebracht ist, sollte die abgeleitete Klasse auch die Medien Zeiten festlegen, indem Sie die [**imediasample:: setmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) -Methode aufruft. Weitere Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

Gibt "S \_ false" am Ende des Streams zurück. Dies bewirkt, dass die **csourcestream** -Klasse das Ende der Stream-Benachrichtigung sendet und die Puffer Verarbeitungs Schleife stoppt. Weitere Informationen finden Sie unter [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




