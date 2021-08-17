---
description: Gibt Dem Qualitätsmanager Feedback zur Wiedergabequalität.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: MEQualityNotify-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd019db55a0791ec5464cf67c7ee4d3e4a86f918efc2b4e87f4ddde2f3574ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061875"
---
# <a name="mequalitynotify-event"></a>MEQualityNotify-Ereignis

Gibt Dem Qualitätsmanager Feedback zur Wiedergabequalität.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE           | Beschreibung                         |
|-------------------|-------------------------------------|
| VT \_ I8<br/> | Siehe Hinweise.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von einigen Pipelinekomponenten ausgelöst. Die Mediensitzung gibt das Ereignis an den Qualitäts-Manager weiter, indem die [**METHODE VORGESETZTEQualityManager::NotifyQualityEvent aufgerufen**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) wird.

Der erweiterte Typ des Ereignisses gibt die Bedeutung der Ereignisdaten an.



| Erweiterter Typ                            | Ereignisdaten                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ QUALITY \_ NOTIFY \_ PROCESSING \_ LATENCY | Die von der Komponente eingeführte ungefähre Verarbeitungslatenz in Einheiten von 100 Nanosekunden.<br/> Verarbeitungslatenz ist die Latenz, die eine Komponente in die Pipeline einläuft, indem sie ein Beispiel verarbeitet. In einigen Fällen kann die Latenz nicht einfach abgeleitet werden, indem die Aufrufe von [**ZUDRQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) und [**ZUDRQualityManager::NotifyProcessOutput betrachtet werden.**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput) Beispielsweise gibt es möglicherweise keine 1:1-Entsprechung zwischen Eingabe- und Ausgabebeispielen. In diesem Fall kann die Komponente ein MEQualityNotify-Ereignis mit der Verarbeitungslatenz senden. Wenn sich die Verarbeitungslatenz ändert, kann die Komponente während des Streamings jederzeit ein neues Ereignis senden.<br/> |
| MF \_ QUALITY \_ NOTIFY \_ SAMPLE \_ LAG         | Verzögerungszeit für das Beispiel in Einheiten von 100 Nanosekunden. Wenn der Wert positiv ist, war die Stichprobe zu spät. Wenn der Wert negativ ist, war die Stichprobe früh.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Um den erweiterten Typ zu erhalten, rufen [**Sie DANNMediaEvent::GetExtendedType auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)

Pipelinekomponenten sind zum Senden dieses Ereignisses nicht erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VERERBungsqualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




