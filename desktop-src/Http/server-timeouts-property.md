---
title: Servertimeouts-Eigenschaft
description: Servertimeouts-Eigenschaft
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- Http-Eigenschaft "Servertimeouts"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd0495950a83ba2e675fc5b89efd33d3c53c90e0c21ad306d5845b6bafae324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562470"
---
# <a name="server-timeouts-property"></a>Servertimeouts-Eigenschaft

Mit der HTTP-Server-API können Anwendungen die Timeoutlimits für Serververbindungen für eine Serversitzung oder eine URL-Gruppe festlegen. Die HTTP-Timeouts-Eigenschaft wird verwendet, um alle Timeouts anwendungsspezifisch festzulegen. Die **Timer IdleConnection** und **HeaderWait** können auch ÜBER DIE HTTP-Server-API konfiguriert werden. Wenn die Timer für die GESAMTE HTTP-Server-API konfiguriert sind, gelten sie für alle HTTP-Server-API-Anwendungen auf dem Computer, und die Einstellungen bleiben erhalten, wenn der Dienst neu gestartet wird.

Weitere Informationen zum Konfigurieren von Timern finden Sie unter [Konfigurieren der anwendungsspezifischen Timeouts.](configuring-the-application-specific-timeouts.md)

Wenn die Timer nicht für eine URL-Gruppe oder Serversitzung konfiguriert sind, gelten die Standardkonfigurationen der HTTP-Server-API.

Die Reihenfolge der Timeouterzwingung lautet wie folgt:

1.  Die HTTP-Server-API-weiten Standardwerte gelten für alle HTTP-Server-API-Anwendungen auf dem Computer.
2.  Die Serversitzungstimeouts überschreiben die HTTP-Server-API-weiten Einstellungen, wenn sie festgelegt sind.
3.  Die URL-Gruppeneinstellungen setzen die Serversitzungskonfigurationen außer Kraft, wenn sie festgelegt sind.

In der folgenden Tabelle sind die Standardlimits für Verbindungstimeouts aufgeführt.



| Timer           | Definition                                                                                                        | HTTP-Server-API-Standard | Konfigurierbar als HTTP-Server-API-Wide | Konfigurierbar als anwendungsspezifisch |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | Die Verbindung ist während des Leerlaufs abgelaufen.                                                                        | 120 s                 | Ja                                  | Eingeschränkt                              |
| HeaderWait      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass die HTTP-Server-API den Header analysiert.                                 | 120 s                 | Ja                                  | Eingeschränkt                              |
| EntityBody      | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass der Anforderungsentitätstext eintrifft.                                       | 120 s                 | Nein                                   | Ja                                  |
| DrainEntityBody | Die Verbindung ist abgelaufen, während darauf gewartet wird, dass die HTTP-Server-API den Entitätstext auf einer Keep-Alive Verbindung leert. | 120 s                 | Nein                                   | Ja                                  |
| MinSendRate     | Die Verbindung ist abgelaufen, da die Antwortsenderrate langsamer war als der Standardwert von 150 Bytes/s.               | 150 s                 | Nein                                   | Ja                                  |
| Anforderungswarteschlange    | Die Verbindung ist abgelaufen, da die Anforderung in der Anforderungswarteschlange verblieb, bevor sie von der Anwendung übernommen wurde.     | 120 Bytes/s           | Nein                                   | Ja                                  |



 

 

 




