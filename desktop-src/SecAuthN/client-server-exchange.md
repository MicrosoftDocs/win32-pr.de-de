---
description: Client-/Server-Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Client-/Server-Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131060"
---
# <a name="clientserver-exchange"></a>Client-/Server-Exchange

Wenn ein Benutzer ein Ticket für einen Server hat, kann der Arbeitsstations Client eine sichere Kommunikationssitzung mit diesem Server einrichten.

**So richten Sie eine sichere Kommunikationssitzung mit einem Server ein**

1.  Der Client sendet dem Server eine Nachricht vom Typ krb \_ AP \_ req (Kerberos-Anwendungsanforderung). Diese Nachricht enthält eine Authentifikator-Nachricht, die mit dem Schlüssel verschlüsselt ist, der vom [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) für die Sitzung mit dem Server gesendet wird, das Ticket für Sitzungen mit dem Server und ein Flag, das angibt, ob der Client die gegenseitige Authentifizierung anfordert. Das Festlegen des Flags, das die gegenseitige Authentifizierung anfordert, ist eine der Optionen beim Konfigurieren von [*Kerberos*](/windows/desktop/SecGloss/k-gly). Der Benutzer wird nie gefragt, ob eine gegenseitige Authentifizierung verwendet werden soll.
2.  Der Server empfängt krb \_ AP \_ req, entschlüsselt das Ticket und extrahiert die Autorisierungs Daten des Benutzers und den [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly).
3.  Der Server verwendet den Sitzungsschlüssel aus dem Ticket zum Entschlüsseln der Authentifikator-Nachricht des Benutzers und wertet den Zeitstempel in aus.
4.  Wenn die Authentifikator-Nachricht gültig ist, überprüft der Server das Flag für die gegenseitige Authentifizierung in der Client Anforderung.
5.  Wenn das Flag für die gegenseitige Authentifizierung festgelegt ist, verwendet der Server den Sitzungsschlüssel, um die Uhrzeit aus der Authentifikator-Nachricht des Benutzers zu verschlüsseln, und gibt das Ergebnis in einer Nachricht vom Typ krb \_ AP \_ Rep (Kerberos-Anwendungs Antwort) zurück.
6.  Wenn der Client krb \_ AP \_ Rep empfängt, entschlüsselt er die Authenticator-Nachricht des Servers mit dem Sitzungsschlüssel, den er mit dem Server freigibt, und vergleicht die vom Dienst zurück gesendete Zeit mit dem Zeitpunkt in der ursprünglichen authentifikatornachricht. Wenn Sie einander entsprechen, ist der Client sicher, dass der Dienst echt ist und die Verbindung fortgesetzt wird.

 

 
