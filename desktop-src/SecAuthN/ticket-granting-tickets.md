---
description: Da das Kerberos-Protokoll ursprünglich entworfen wurde, wurde ein Hauptschlüssel für einen Benutzer von einem vom Benutzer bereitgestellten Kennwort abgeleitet.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Ticket-Granting Tickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd56ef05ce2ea9149b9bd35ef17dc684973f7125026f474e5a8dd3d1d14ff4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916382"
---
# <a name="ticket-granting-tickets"></a>Ticket-Granting Tickets

Da das [*Kerberos-Protokoll*](../secgloss/k-gly.md) ursprünglich entworfen wurde, wurde ein Hauptschlüssel für einen Benutzer von einem vom Benutzer bereitgestellten Kennwort abgeleitet. Wenn sich ein Benutzer angemeldet hat, akzeptierte der Kerberos-Client auf der Arbeitsstation des Benutzers das Kennwort des Benutzers und konvertierte es in einen Verschlüsselungsschlüssel, indem er den Text über eine one-way-Hashfunktion [*übergeben*](../secgloss/h-gly.md) hat. Der resultierende Hash war der [*Hauptschlüssel des Benutzers.*](../secgloss/m-gly.md) Der Client hat diesen *Hauptschlüssel verwendet,* um [*sitzungsschlüssel zu entschlüsseln, die vom*](../secgloss/s-gly.md) KDC empfangen wurden.

Das Problem beim ursprünglichen Kerberos-Entwurf ist, dass der Client jedes Mal, wenn er einen Sitzungsschlüssel aus dem KDC entschlüsselt, den Hauptschlüssel des Benutzers benötigt. Dies bedeutet, dass der Client den Benutzer am Anfang jedes Client-/Serveraustauschs nach dem Kennwort fragen muss, oder der Client muss den Benutzerschlüssel auf der Arbeitsstation speichern. Häufige Unterbrechungen des Benutzers sind zu intrusiv. Beim Speichern des Schlüssels auf der Arbeitsstation besteht die Gefahr, dass ein Schlüssel, der aus dem Benutzerkennwort abgeleitet ist, beeinträchtigt wird. Dies ist ein langfristiger Schlüssel.

Die Lösung dieses Problems durch das Kerberos-Protokoll ist, dass der Client einen temporären Schlüssel vom KDC bekommt. Dieser temporäre Schlüssel ist nur für diese [*Anmeldesitzung gut.*](../secgloss/l-gly.md) Wenn sich ein Benutzer anmeldet, fordert der Client ein Ticket für das KDC genauso an wie ein Ticket für jeden anderen Dienst. Der KDC antwortet, indem er einen Anmeldesitzungsschlüssel und ein Ticket für einen speziellen Server erstellt, den vollständigen Ticketgewährungsdienst des KDC. Eine Kopie des Anmeldesitzungsschlüssels ist in das Ticket eingebettet, und das Ticket wird mit dem Hauptschlüssel des KDC verschlüsselt. Eine weitere Kopie des Anmeldesitzungsschlüssels wird mit dem Hauptschlüssel des Benutzers verschlüsselt, der vom Anmeldekennwort des Benutzers abgeleitet wurde. Sowohl das Ticket als auch der verschlüsselte Sitzungsschlüssel werden an den Client gesendet.

Wenn der Client die Antwort des KDC erhält, entschlüsselt er den Anmeldesitzungsschlüssel mit dem Hauptschlüssel des Benutzers, der vom Kennwort des Benutzers abgeleitet wurde. Der Client benötigt den vom Benutzerkennwort abgeleiteten Schlüssel nicht mehr, da der Client jetzt den Anmeldesitzungsschlüssel verwendet, um seine Kopie eines beliebigen Serversitzungsschlüssels zu entschlüsseln, den er vom KDC erhält. Der Client speichert den Anmeldesitzungsschlüssel zusammen mit seinem Ticket für den vollständigen Ticketgewährungsdienst des KDC im Ticketcache.

Das Ticket für den vollständigen Ticketgewährungsdienst wird als Ticket granting ticket (TGT) bezeichnet. Wenn der Client das KDC um ein Ticket für einen Server bittet, stellt er Anmeldeinformationen [*in*](../secgloss/c-gly.md) Form einer Authentatormeldung und eines Tickets (in diesem Fall ein TGT) wie anmeldeinformationen für jeden anderen Dienst vor. Der Ticketgewährungsdienst öffnet das TGT mit seinem Hauptschlüssel, extrahiert den Anmeldesitzungsschlüssel für diesen Client und verwendet den Anmeldesitzungsschlüssel, um die Kopie eines Sitzungsschlüssels des Clients für den Server zu verschlüsseln.

 

 
