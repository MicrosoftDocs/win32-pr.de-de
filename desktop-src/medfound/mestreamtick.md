---
description: Signalisiert, dass in einem Medienstream zu einem bestimmten Zeitpunkt keine Daten verfügbar sind.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: MEStreamTick-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b72a61964e296ac5f7aa69eb2be6773b622f7b44df8300affa0150af2f8a77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974059"
---
# <a name="mestreamtick-event"></a>MEStreamTick-Ereignis

Signalisiert, dass in einem Medienstream zu einem bestimmten Zeitpunkt keine Daten verfügbar sind.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE           | BESCHREIBUNG                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | Die Zeit, zu der die Lücke auftritt , in Einheiten von 100 Nanosekunden.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis signalisiert eine Lücke in den Daten. Das Ereignis benachrichtigt downstream-Komponenten, dass zum angegebenen Zeitpunkt keine Daten erwartet werden.

Das Ereignis sollte von dem Objekt gesendet werden, das die Zeitstempel für die Medienbeispiele im Stream generiert. Je nach Format der Daten ist dies entweder:

-   Der Medienstream auf der Medienquelle [**(BENUTZEROBERFLÄCHEMediaStream-Schnittstelle)**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) oder
-   Die Decodertransformation ([**DIETRANSFORM-Schnittstelle).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Während der Lücke sollte das Objekt das Ereignis ungefähr so oft senden, wie es normalerweise Stichproben erzeugen würde. Senden Sie für Videos ein Ereignis für jeden fehlenden Frame. Senden Sie für Audiodaten das Ereignis mindestens einmal pro Sekunde während der Lücke. Der Wert des Ereignisses ist der Zeitstempel der fehlenden Stichprobe. Senden Sie so viele MEStreamTick-Ereignisse wie erforderlich, um die Lücke in den Daten zu füllen.

Wenn eine Medienquelle über mehrere Datenströme verfügt und in mehr als einem Stream eine Lücke besteht, sollte jeder Stream MEStreamTick-Ereignisse senden. Wenn beispielsweise eine Lücke in Audio- und Videodaten besteht, senden beide Datenströme das Ereignis.

Das MEStreamTick-Ereignis schließt keine [**NSBMediaStream::RequestSample-Anforderung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) ab. Die Medienquelle muss weiterhin ein [MEMediaSample-Ereignis](memediasample.md) für jeden Aufruf von **RequestSample senden.**

Mediensenken können dieses Ereignis nicht direkt nutzen. Um eine Lücke im Stream zu einer Mediensenke zu signalisieren, rufen [**Sie DENTSTREAMSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) mit einem **MFSTREAMSINK \_ MARKER \_ TICK-Marker** auf. Die Media Foundation-Pipeline konvertiert MEStreamTick-Ereignisse bei Bedarf in **MFSTREAMSINK \_ MARKER \_ TICK-Marker.**

Legen Sie das [**MFSampleExtension \_ Discontinuity-Attribut**](mfsampleextension-discontinuity-attribute.md) nicht für das nächste Medienbeispiel nach einem MEStreamTick-Ereignis fest. Das **MFSampleExtension \_ Discontinuity-Attribut** impliziert, dass der Zeitstempel gegenüber vorherigen Zeitstempeln diskontinuierlich ist, während MEStreamTick impliziert, dass Zeitstempel fortlaufend sind, aber einige Daten fehlen.

> [!Note]  
> In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass das Beispiel nach einem MEStreamTick-Ereignis das [**Attribut MFSampleExtension \_ Discontinuity enthalten**](mfsampleextension-discontinuity-attribute.md) sollte.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




