---
description: Signalisiert, dass für einen Mediendaten Strom keine Daten zu einem angegebenen Zeitpunkt verfügbar sind.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Mestreamtick-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372870"
---
# <a name="mestreamtick-event"></a>Mestreamtick-Ereignis

Signalisiert, dass für einen Mediendaten Strom keine Daten zu einem angegebenen Zeitpunkt verfügbar sind.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | Der Zeitpunkt, zu dem die Lücke auftritt, in 100-Nanosecond-Einheiten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis signalisiert eine Lücke in den Daten. Das Ereignis benachrichtigt Downstreamkomponenten, dass zum angegebenen Zeitpunkt keine Daten erwartet werden.

Das Ereignis sollte von dem Objekt gesendet werden, das die Zeitstempel für die Medien Beispiele im Stream generiert. Abhängig vom Format der Daten ist dies entweder:

-   Der Mediendaten Strom in der Medienquelle ([**IMF Mediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle) oder
-   Die decodertransformation ([**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle).

Während der Lücke sollte das Objekt das Ereignis so oft senden, wie es normalerweise Beispiele erzeugt. Senden Sie für ein Video ein Ereignis für jeden fehlenden Frame. Senden Sie das Ereignis für Audiodaten mindestens einmal pro Sekunde während der Lücke. Der Wert des Ereignisses ist der Zeitstempel der fehlenden Stichprobe. Senden Sie beliebig viele mestreamtick-Ereignisse, um die Lücke in den Daten zu füllen.

Wenn eine Medienquelle über mehrere Datenströme verfügt und eine Lücke in mehr als einem Stream besteht, sollte jeder Stream mestreamtick-Ereignisse senden. Wenn beispielsweise eine Lücke in den Audio-und Videodaten vorliegt, senden beide Streams das Ereignis.

Das mestreamtick-Ereignis schließt eine [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Anforderung nicht ab. Die Medienquelle muss weiterhin ein [memediasample](memediasample.md) -Ereignis für jeden **requestsample**-Anforderer senden.

Medien senken können dieses Ereignis nicht direkt verarbeiten. Um eine Lücke im Stream an eine Medien Senke zu signalisieren, nennen Sie [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) mit einem **mfstreamsink- \_ markermarker \_** . Bei Bedarf werden von der Media Foundation Pipeline mestreamtick-Ereignisse in **mfstreamsink- \_ \_ markermarker** konvertiert.

Legen Sie das Attribut " [**\_ discontinuity" der MF SampleExtension**](mfsampleextension-discontinuity-attribute.md) -Eigenschaft nicht auf das nächste Medien Beispiel nach einem mestreamtick-Ereignis fest. Das Attribut " **mfsampleextension \_ discontinuity** " impliziert, dass der Zeitstempel mit vorherigen Zeitstempeln diskontinuierlich ist, wohingegen "mestreamtick" impliziert, dass Zeitstempel kontinuierlich sind, aber einige Daten fehlen.

> [!Note]  
> In einer früheren Version der Dokumentation wurde fälschlicherweise angegeben, dass das Beispiel nach einem mestreamtick-Ereignis das Attribut " [**MF SampleExtension \_ discontinuity**](mfsampleextension-discontinuity-attribute.md) " aufweisen sollte.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




