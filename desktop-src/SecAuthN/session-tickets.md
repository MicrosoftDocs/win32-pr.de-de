---
description: Anstatt die verschlüsselten Sitzungsschlüssel an beide Prinzipale zu senden, sendet das KDC sowohl die Kopien des Client- als auch des Servers des Sitzungsschlüssels an den Client.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Sitzungstickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b514abc76eabcbe70f00c1e879b9389c83ad333d7b5c10d4150478f03db6a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918069"
---
# <a name="session-tickets"></a>Sitzungstickets

Anstatt die verschlüsselten Sitzungsschlüssel an beide Prinzipale zu senden, sendet das [KDC](key-distribution-center.md) sowohl [](../secgloss/s-gly.md) die Kopien des Client- als auch des Servers des Sitzungsschlüssels an den Client. Die Kopie des Sitzungsschlüssels des Clients wird [](../secgloss/m-gly.md) mit dem Hauptschlüssel des Clients verschlüsselt und kann daher nicht von einer anderen Entität entschlüsselt werden. Die Kopie des Sitzungsschlüssels des Servers wird zusammen mit Autorisierungsdaten zum Client in eine Datenstruktur eingebettet, die als Ticket bezeichnet wird. Das Ticket wird vollständig mit dem Hauptschlüssel des Servers verschlüsselt und kann daher nicht vom Client oder einer anderen Entität gelesen oder geändert werden, die keinen Zugriff auf den Hauptschlüssel des Servers hat. Es liegt in der Verantwortung des Clients, das Ticket sicher zu speichern, bis der Kontakt mit dem Server besteht.

> [!Note]  
> Das KDC stellt nur einen Ticketgewährungsdienst zur Verfügung. Client und Server sind dafür verantwortlich, die jeweiligen Hauptschlüssel sicher zu halten.

 

Wenn der Client die Antwort des KDC empfängt, extrahiert er das Ticket und seine eigene Kopie des Sitzungsschlüssels und speichert beide in einem sicheren Cache. Um eine sichere Sitzung mit dem Server herzustellen, sendet er dem Server eine Nachricht, die aus [](authenticator-messages.md) dem Ticket besteht, noch mit dem Hauptschlüssel des Servers verschlüsselt ist, und einer Authentatornachricht, die mit dem Sitzungsschlüssel verschlüsselt ist. Zusammen sind das Ticket und die Authentatornachricht die Anmeldeinformationen des Clients [*für*](../secgloss/c-gly.md) den Server.

Wenn der Server Anmeldeinformationen von einem Client empfängt, entschlüsselt [](../secgloss/s-gly.md)er das Ticket mit seinem Hauptschlüssel, [](../secgloss/m-gly.md)extrahiert den Sitzungsschlüssel und verwendet den Sitzungsschlüssel, um die Authentatornachricht des Clients zu entschlüsseln. Wenn alles überprüft wird, weiß der Server, dass die Anmeldeinformationen des Clients vom KDC ausgestellt wurden, einer vertrauenswürdigen Autorität. Für die gegenseitige Authentifizierung antwortet der Server, indem er den Zeitstempel aus der Authentisierungsnachricht des Clients mithilfe des Sitzungsschlüssels verschlüsselt. Diese verschlüsselte Nachricht wird an den Client gesendet. Der Client entschlüsselt dann die Nachricht. Wenn die zurückgegebene Nachricht mit dem Zeitstempel in der ursprünglichen Authentitätsmeldung identisch ist, wird der Server authentifiziert.

Als zusätzlichen Vorteil muss der Server die Sitzungsschlüssel, die er verwendet, nicht mit seinen Clients speichern. Jeder Client ist dafür verantwortlich, das Ticket für den Server im Ticketcache zu verwalten und bei jedem Zugriff auf den Server zu präsentieren. Wenn der Server ein Ticket von einem Client empfängt, verwendet er seinen Hauptschlüssel, um das Ticket zu entschlüsseln und den Sitzungsschlüssel zu extrahieren. Wenn der Server den Sitzungsschlüssel nicht mehr benötigt, wird der Schlüssel gelöscht.

Der Client muss nicht jedes Mal auf das KDC zugreifen, wenn er Zugriff auf diesen bestimmten Server möchte. Tickets können wiederverwendet werden. Als Vorsichtsmaßnahme gegen die Möglichkeit eines Ticketdiebstahls haben Tickets eine Ablaufzeit, die vom KDC in der Ticketstruktur angegeben wird. Wie lange ein Ticket gültig ist, hängt von der Kerberos-Richtlinie für den Bereich ab. In der Regel sind Tickets nicht länger als acht Stunden gut, ungefähr so lange wie eine normale [*Anmeldesitzung.*](../secgloss/l-gly.md) Wenn sich der Benutzer auf einer Clientarbeitsstation abmeldet, wird der Clientticketcache geleert, und alle Tickets und Clientsitzungsschlüssel werden zerstört.

 

 
