---
description: Die DoBufferProcessingLoop-Methode generiert Mediendaten und übermittelt sie an den nachgeschalteten Eingabepin.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: CSourceStream.DoBufferProcessingLoop-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d23df592abd125fd64362af89b6f81c5e9dcc20f0aa6cc998974a8fd2d4d87f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953739"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>CSourceStream.DoBufferProcessingLoop-Methode

Die `DoBufferProcessingLoop` -Methode generiert Mediendaten und übermittelt sie an den nachgeschalteten Eingabepin.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Thread hat eine Beendigungsanforderung empfangen.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Stream wurde beendet, oder der Downstreamfilter akzeptiert keine Beispiele.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode implementiert die Hauptschleife, die Daten verarbeitet und nachgeschaltet übermittelt. Jedes Mal, wenn die Schleife durchlaufen wird, ruft die -Methode ein leeres Medienbeispiel aus der Zuweisung ab. Das Beispiel wird an die [**CSourceStream::FillBuffer-Methode**](csourcestream-fillbuffer.md) übergeben. Die **FillBuffer-Methode,** die die abgeleitete Klasse implementieren muss, generiert Mediendaten und platziert sie im Beispielpuffer.

Die Schleife endet, wenn eine der folgenden Vorgänge auftritt:

-   Die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) des Eingabepins lehnt ein Beispiel ab.
-   Die **FillBuffer-Methode** gibt S \_ FALSE zurück, was das Ende des Streams angibt, oder gibt einen Fehlercode zurück.
-   Der Thread empfängt eine [**CSourceStream::Stop-Anforderung.**](csourcestream-stop.md)

Die `DoBufferProcessingLoop` -Methode verarbeitet die End-of-Stream-Benachrichtigung. Wenn ein Fehler auftritt, wird ein [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) an den Filtergraph-Manager gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




