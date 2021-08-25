---
title: Clientanwendungsrückruffunktionen
description: Zwei Arten von Rückrufsignaturen.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977100"
---
# <a name="client-application-callback-functions"></a>Clientanwendungsrückruffunktionen

Das Windows Biometric Framework unterstützt zwei Arten von Rückrufsignaturen. Ab Windows 8 wird der folgende Rückruf unterstützt. Es wird empfohlen, diesen Rückruf für alle neuen Anwendungen zu implementieren. Dieser Rückruf kann jedoch nicht in Windows 7 verwendet werden.



| Rückruf                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PWINBIO \_ ASYNC \_ COMPLETION \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Benachrichtigt die Clientanwendung, dass ein asynchroner Vorgang, der mit [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) oder [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) gestartet wurde, abgeschlossen wurde.<br/> |



 

Die folgenden Rückruffunktionen wurden in Windows 7 eingeführt. Es wird empfohlen, sie nicht für neue Anwendungen zu implementieren, die auf Windows 8 und höhere Betriebssysteme ausgerichtet sind.



| Rückruf                                                                                 | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PWINBIO \_ CAPTURE \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Gibt Ergebnisse der asynchronen [**WinBioCaptureSampleWithCallback-Funktion zurück.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback)<br/> |
| [**PWINBIO \_ ENROLL \_ CAPTURE \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Gibt Ergebnisse der [**asynchronen WinBioEnrollCaptureWithCallback-Funktion zurück.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback)<br/> |
| [**\_PWINBIO-EREIGNISRÜCKRUF \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Gibt Ergebnisse der asynchronen [**WinBioRegisterEventMonitor-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) zurück.<br/>           |
| [**PWINBIO \_ IDENTIFY \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Gibt Ergebnisse der asynchronen [**WinBioIdentifyWithCallback-Funktion zurück.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback)<br/>           |
| [**\_PWINBIO– \_ \_ SENSORRÜCKRUF SUCHEN**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Gibt Ergebnisse der asynchronen [**WinBioLocateSensorWithCallback-Funktion zurück.**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback)<br/>   |
| [**PWINBIO \_ VERIFY \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Gibt Ergebnisse der asynchronen [**WinBioVerifyWithCallback-Funktion zurück.**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)<br/>               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientanwendungsreferenz](client-application-reference.md)
</dt> </dl>

 

 





