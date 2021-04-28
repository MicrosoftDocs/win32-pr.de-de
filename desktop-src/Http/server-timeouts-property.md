---
title: Server timeouts-Eigenschaft
description: Server timeouts-Eigenschaft
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Http-Eigenschaft "Server timeouts"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26fcd1376e8b7394a3a037bbbe00495466e32609
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090858"
---
# <a name="server-timeouts-property"></a>Server timeouts-Eigenschaft

Mit der HTTP-Server-API können Anwendungen die Serververbindungs-Timeoutlimits für eine Serversitzung oder eine URL-Gruppe festlegen. Mit der HTTP-Timeouteigenschaft werden alle Timeouts anwendungsspezifisch festgelegt. Die **Timer IdleConnection** **und HeaderWait** können auch API-weit für HTTP-Server konfiguriert werden. Wenn die Timer für die HTTP-Server-API konfiguriert sind, gelten sie für alle HTTP Server-API-Anwendungen auf dem Computer, und die Einstellungen bleiben erhalten, wenn der Dienst neu gestartet wird.

Weitere Informationen zum Konfigurieren von Timern finden Sie unter [Configuring the Application Specific Timeouts](configuring-the-application-specific-timeouts.md).

Wenn die Timer nicht für eine URL-Gruppe oder Serversitzung konfiguriert sind, gelten die Standardkonfigurationen der HTTP-Server-API.

Die Reihenfolge der Timeouterzwingung lautet wie folgt:

1.  Die API-weiten Standardeinstellungen für HTTP-Server gelten für alle HTTP Server-API-Anwendungen auf dem Computer.
2.  Die Serversitzungs-Timeouts setzen die API-weiten HTTP-Servereinstellungen außer Kraft, wenn sie festgelegt sind.
3.  Die URL-Gruppeneinstellungen überschreiben die Serversitzungskonfigurationen, wenn sie festgelegt sind.

In der folgenden Tabelle sind die Standardlimits für Verbindungszeitlimits aufgeführt.



| Timer           | Definition                                                                                                        | HTTP-Server-API-Standard | Konfigurierbar als HTTP-Server-API | Konfigurierbar als anwendungsspezifisch |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | Die Verbindung ist abgelaufen, während sie im Leerlauf bleibt.                                                                        | 120 s                 | Ja                                  | Eingeschränkt                              |
| HeaderWait      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass die HTTP-Server-API den Header analysiert.                                 | 120 s                 | Ja                                  | Eingeschränkt                              |
| EntityBody      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass der Anforderungsentitätstext eintrifft.                                       | 120 s                 | Nein                                   | Ja                                  |
| DrainEntityBody | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass die HTTP-Server-API den Entitätstext auf einer Keep-Alive Verbindung leert. | 120 s                 | Nein                                   | Ja                                  |
| MinSendRate     | Die Verbindung ist abgelaufen, da die Antwortsenderrate langsamer war als der Standardwert von 150 Bytes/s.               | 150 s                 | Nein                                   | Ja                                  |
| Anforderungswarteschlange    | Die Verbindung ist abgelaufen, da die Anforderung in der Anforderungswarteschlange verblieb, bevor sie von der Anwendung übernommen wurde.     | 120 Bytes/s           | Nein                                   | Ja                                  |



 

 

 




