---
description: Die FillBuffer-Methode füllt ein Medienbeispiel mit Daten auf.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: CSourceStream.FillBuffer-Methode (Source.h)
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
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687400"
---
# <a name="csourcestreamfillbuffer-method"></a>CSourceStream.FillBuffer-Methode

Die `FillBuffer` -Methode füllt ein Medienbeispiel mit Daten auf.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                             | Beschreibung              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Ende des Streams<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg<br/>       |



 

## <a name="remarks"></a>Hinweise

Die abgeleitete Klasse muss diese Methode implementieren.

Das dieser Methode gegebene Medienbeispiel verfügt über keine Zeitstempel. Die abgeleitete Klasse sollte die [**IMediaSample::SetTime-Methode aufrufen,**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) um die Zeitstempel zu festlegen. Wenn dies für den Medientyp geeignet ist, sollte die abgeleitete Klasse auch die Medienzeiten festlegen, indem sie die [**IMediaSample::SetMediaTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) aufruft. Weitere Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

Gibt S \_ FALSE am Ende des Streams zurück. Dies bewirkt, dass **die CSourceStream-Klasse** die Benachrichtigung zum Ende des Streams sendet und die Pufferverarbeitungsschleife anzuhalten. Weitere Informationen finden Sie unter [**CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




