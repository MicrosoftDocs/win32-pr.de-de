---
description: Bietet dem Quality Manager Feedback zur Wiedergabequalität.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Mequalitynotify-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528271"
---
# <a name="mequalitynotify-event"></a>Mequalitynotify-Ereignis

Bietet dem Quality Manager Feedback zur Wiedergabequalität.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                         |
|-------------------|-------------------------------------|
| VT \_ I8<br/> | Siehe Hinweise.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von einigen Pipeline Komponenten ausgelöst. Die Medien Sitzung leitet das Ereignis an den Quality Manager weiter, indem die [**imfqualitymanager:: notifyqualityevent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) -Methode aufgerufen wird.

Der erweiterte Typ des Ereignisses gibt die Bedeutung der Ereignisdaten an.



| Erweiterter Typ                            | Ereignisdaten                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verarbeitungs Wartezeit für die MF- \_ Qualität \_ Benachrichtigen \_ \_ | Ungefähre Verarbeitungs Wartezeit, die von der Komponente eingeführt wurde, in 100-Nanosecond-Einheiten.<br/> Verarbeitungs Latenz ist die Latenzzeit, die eine Komponente in die Pipeline einführt, indem ein Beispiel verarbeitet wird. In einigen Fällen kann die Wartezeit nicht einfach durch Betrachtung der Aufrufe von [**imfqualitymanager:: notifyprocessinput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) und [**imfqualitymanager:: notifyprocessoutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)abgeleitet werden. Beispielsweise gibt es möglicherweise keine 1:1-Entsprechung zwischen Eingabe Beispielen und Ausgabe Beispielen. In diesem Fall sendet die Komponente möglicherweise ein mequalitynotify-Ereignis mit der Verarbeitungs Latenz. Wenn die Verarbeitungs Latenz geändert wird, kann die Komponente während des Streamings jederzeit ein neues Ereignis senden.<br/> |
| Beispiel Verzögerung für die MF- \_ Qualitäts \_ Benachrichtigung \_ \_         | Verzögerungszeit für das Beispiel in 100-Nanosecond-Einheiten. Wenn der Wert positiv ist, war das Beispiel spät. Wenn der Wert negativ ist, war das Beispiel früh.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Um den erweiterten Typ abzurufen, nennen Sie [**imfmediaevent:: getextendedtype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

Pipeline Komponenten sind nicht erforderlich, um dieses Ereignis zu senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF-Manager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




