---
description: Client-/Server-Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Client-/Server-Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2401d3cf2bb59586e608bc7566c13009869d2874a1532b659f70c6c4e09e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141173"
---
# <a name="clientserver-exchange"></a>Client-/Server-Exchange

Nachdem ein Benutzer über ein Ticket für einen Server verfügt, kann der Arbeitsstationsclient eine sichere Kommunikationssitzung mit diesem Server einrichten.

**So richten Sie eine sichere Kommunikationssitzung mit einem Server ein**

1.  Der Client sendet dem Server eine Nachricht vom Typ KRB \_ AP \_ REQ (Kerberos Application Request). Diese Nachricht enthält eine Authentifikatornachricht, die mit dem Schlüssel verschlüsselt ist, der vom [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) für die Sitzung mit dem Server gesendet wird, das Ticket für Sitzungen mit dem Server und ein Flag, das angibt, ob der Client gegenseitige Authentifizierung anfordert. Das Festlegen des Flags, das gegenseitige Authentifizierung anfordert, ist eine der Optionen beim Konfigurieren von [*Kerberos.*](/windows/desktop/SecGloss/k-gly) Der Benutzer wird nie gefragt, ob die gegenseitige Authentifizierung verwendet werden soll.
2.  Der Server empfängt die \_ KRB-AP-REQ, \_ entschlüsselt das Ticket und extrahiert die Autorisierungsdaten des Benutzers und den [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly).
3.  Der Server verwendet den Sitzungsschlüssel aus dem Ticket, um die Authentifikatornachricht des Benutzers zu entschlüsseln, und wertet den darin enthaltenen Zeitstempel aus.
4.  Wenn die Authentifikatornachricht gültig ist, überprüft der Server das gegenseitige Authentifizierungsflag in der Anforderung des Clients.
5.  Wenn das Gegenseitige Authentifizierungsflag festgelegt ist, verwendet der Server den Sitzungsschlüssel, um die Zeit aus der Authentifikatornachricht des Benutzers zu verschlüsseln, und gibt das Ergebnis in einer Nachricht vom Typ KRB \_ AP \_ REP (Kerberos Application Reply) zurück.
6.  Wenn der Client KRB \_ AP \_ REP empfängt, entschlüsselt er die Authentifikatornachricht des Servers mit dem Sitzungsschlüssel, den er für den Server freigibt, und vergleicht die vom Dienst zurückgesendete Zeit mit der Zeit in der ursprünglichen Authentifikatornachricht. Wenn sie übereinstimmen, ist der Client sicher, dass der Dienst echt ist, und die Verbindung wird fortgesetzt.

 

 
