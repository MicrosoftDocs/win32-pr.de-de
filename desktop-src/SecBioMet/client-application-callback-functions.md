---
title: Rückruf Funktionen für Client Anwendungen
description: Zwei Arten von Rückruf Signaturen.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388610"
---
# <a name="client-application-callback-functions"></a>Rückruf Funktionen für Client Anwendungen

Der Windows-Biometrieframework unterstützt zwei Arten von Rückruf Signaturen. Ab Windows 8 wird der folgende Rückruf unterstützt. Es wird empfohlen, dass Sie diesen Rückruf für alle neuen Anwendungen implementieren. Dieser Rückruf kann jedoch in Windows 7 nicht verwendet werden.



| Rückruf                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**pwinbio \_ Async- \_ Abschluss \_ Rückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Benachrichtigt die Client Anwendung, dass ein asynchroner Vorgang, der mithilfe von [**winbioasyncopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) oder [**winbioasyncopenframework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) gestartet wurde, abgeschlossen wurde.<br/> |



 

Die folgenden Rückruf Funktionen wurden in Windows 7 eingeführt. Es wird empfohlen, Sie nicht für neue Anwendungen zu implementieren, die auf Windows 8 und spätere Betriebssysteme abzielen.



| Rückruf                                                                                 | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**pwinbio \_ Capture- \_ Rückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Gibt Ergebnisse aus der asynchronen [**winbiocapturesamplewithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) -Funktion zurück.<br/> |
| [**pwinbio-Registrierungs \_ \_ \_ Rückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Gibt Ergebnisse aus der asynchronen [**winbioregistricapturewithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) -Funktion zurück.<br/> |
| [**pwinbio- \_ Ereignis \_ Rückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Gibt Ergebnisse aus der asynchronen [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion zurück.<br/>           |
| [**pwinbio \_ - \_ identifizrückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Gibt Ergebnisse aus der asynchronen [**winbioidentifywithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) -Funktion zurück.<br/>           |
| [**pwinbio-Abruf \_ \_ Sensor \_ Rückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Gibt Ergebnisse aus der asynchronen [**winbiolotoresensorwithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) -Funktion zurück.<br/>   |
| [**pwinbio \_ - \_ prüfrückruf**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Gibt Ergebnisse aus der asynchronen [**winbioverifywithcallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) -Funktion zurück.<br/>               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client Anwendungs Referenz](client-application-reference.md)
</dt> </dl>

 

 





