---
title: Server Timeouts (Eigenschaft)
description: .
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Server Timeouts-Eigenschaft http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356c1e0d0e9eea2e5db9bf43882f26f9d7e3ddb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388468"
---
# <a name="server-timeouts-property"></a>Server Timeouts (Eigenschaft)

Mit der HTTP-Server-API können Anwendungen die Timeout Grenzwerte für die Server Verbindung für eine Server Sitzung oder eine URL-Gruppe festlegen. Die http-Timeouts-Eigenschaft wird verwendet, um alle Timeouts auf anwendungsspezifischer Basis festzulegen. Der **idleconnection** -und der **headerwait** -Timer können auch http-Server-API-weit konfiguriert werden. Wenn die Timer http-Server-API-weit konfiguriert sind, gelten Sie für alle HTTP-Server-API-Anwendungen auf dem Computer, und die Einstellungen bleiben bestehen, wenn der Dienst neu gestartet wird.

Weitere Informationen zum Konfigurieren von Timern finden Sie unter [Konfigurieren der anwendungsspezifischen Timeouts](configuring-the-application-specific-timeouts.md).

Wenn die Timer nicht für eine URL-Gruppe oder Server Sitzung konfiguriert sind, gelten die Standardkonfigurationen der HTTP-Server-API.

Die Reihenfolge der Timeout Erzwingung lautet wie folgt:

1.  Die API-weiten http-Server-Standardwerte gelten für alle HTTP-Server-API-Anwendungen auf dem Computer.
2.  Die Server Sitzungs Timeouts setzen die HTTP-Server-API-weiten Einstellungen außer Kraft, wenn diese festgelegt sind.
3.  Die URL-Gruppeneinstellungen überschreiben die Server Sitzungs Konfigurationen, wenn diese festgelegt sind.

In der folgenden Tabelle sind die Standard Limits für Verbindungs Timeout aufgeführt.



| Timer           | Definition                                                                                                        | HTTP-Server-API-Standard | Konfigurierbar als HTTP-Server-API Wide | Konfigurierbar als anwendungsspezifisch |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| Idleconnection  | Die Verbindung ist abgelaufen, während der Leerlauf bleibt.                                                                        | 120 Sek.                 | Ja                                  | Eingeschränkt                              |
| Headerwait      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass die HTTP-Server-API den Header analysiert.                                 | 120 Sek.                 | Ja                                  | Eingeschränkt                              |
| EntityBody      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass der Anforderungs Entitäts Text eintrifft.                                       | 120 Sek.                 | Nein                                   | Ja                                  |
| Drainentitybody | Die Verbindung ist abgelaufen, während darauf gewartet wurde, dass die HTTP-Server-API den Entitäts Text auf eine Keep-Alive Verbindung abfließt. | 120 Sek.                 | Nein                                   | Ja                                  |
| Minsendrate     | Die Verbindung ist abgelaufen, weil die Antwort Senderate langsamer als der Standardwert von 150 Bytes/Sek. ist.               | 150 SEK.                 | Nein                                   | Ja                                  |
| Anforderungswarteschlange    | Die Verbindung ist abgelaufen, weil die Anforderung in der Anforderungs Warteschlange verbleibt, bevor Sie von der Anwendung abgerufen wurde.     | 120 Bytes/Sek.           | Nein                                   | Ja                                  |



 

 

 




