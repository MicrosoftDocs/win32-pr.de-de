---
description: Anstatt die verschlüsselten Sitzungsschlüssel an beide Prinzipale zu senden, sendet der KDC sowohl den Client-als auch die Server Kopien des Sitzungsschlüssels an den Client.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Sitzungs Tickets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349392"
---
# <a name="session-tickets"></a>Sitzungs Tickets

Anstatt die verschlüsselten Sitzungsschlüssel an beide Prinzipale zu senden, sendet der [KDC](key-distribution-center.md) sowohl den Client-als auch die Server Kopien des [*Sitzungsschlüssels*](../secgloss/s-gly.md) an den Client. Die Client Kopie des Sitzungsschlüssels wird mit dem [*Hauptschlüssel*](../secgloss/m-gly.md) des Clients verschlüsselt und kann daher von keiner anderen Entität entschlüsselt werden. Die Server Kopie des Sitzungsschlüssels wird zusammen mit den Autorisierungs Daten über den Client in einer Datenstruktur, die als Ticket bezeichnet wird, eingebettet. Das Ticket ist vollständig mit dem Hauptschlüssel des Servers verschlüsselt und kann daher nicht vom Client oder einer anderen Entität gelesen oder geändert werden, die keinen Zugriff auf den Hauptschlüssel des Servers hat. Es liegt in der Verantwortung des Clients, das Ticket sicher zu speichern, bis die Verbindung mit dem Server hergestellt wird.

> [!Note]  
> Der KDC stellt nur einen Dienst zur Ticket Gewährung bereit. Der Client und der Server sind dafür verantwortlich, die entsprechenden Hauptschlüssel sicher zu halten.

 

Wenn der Client die KDC-Antwort empfängt, extrahiert er das Ticket und seine eigene Kopie des Sitzungsschlüssels, wobei beide in einem sicheren Cache abgelegt werden. Zum Einrichten einer sicheren Sitzung mit dem Server wird dem Server eine Nachricht gesendet, die aus dem Ticket besteht, weiterhin mit dem Hauptschlüssel des Servers verschlüsselt ist, und eine [Authentifikator-Nachricht](authenticator-messages.md) , die mit dem Sitzungsschlüssel verschlüsselt ist. Die Ticket-und Authenticator-Nachricht sind die [*Anmelde*](../secgloss/c-gly.md) Informationen des Clients auf dem Server.

Wenn der Server Anmelde Informationen von einem Client empfängt, entschlüsselt er das Ticket mit dem [*Hauptschlüssel*](../secgloss/m-gly.md), extrahiert den [*Sitzungsschlüssel*](../secgloss/s-gly.md)und verwendet den Sitzungsschlüssel zum Entschlüsseln der authentifikatornachricht des Clients. Wenn alles auscheckt, weiß der Server, dass die Anmelde Informationen des Clients von der KDC, einer vertrauenswürdigen Zertifizierungsstelle, ausgestellt wurden. Bei gegenseitiger Authentifizierung antwortet der Server, indem er den Zeitstempel aus der Authentifikator-Nachricht des Clients mithilfe des Sitzungsschlüssels verschlüsselt. Diese verschlüsselte Nachricht wird an den Client gesendet. Der Client entschlüsselt dann die Nachricht. Wenn die zurückgegebene Meldung mit dem Zeitstempel in der ursprünglichen authentifikatornachricht identisch ist, wird der Server authentifiziert.

Ein zusätzlicher Vorteil ist, dass der Server die Sitzungsschlüssel, die er verwendet, nicht mit seinen Clients speichern muss. Es ist für jeden Client zuständig, das Ticket für den Server im Ticket Cache zu verwalten und dieses Ticket bei jedem Zugriff auf den Server zu präsentieren. Wenn der Server ein Ticket von einem Client empfängt, verwendet er seinen Hauptschlüssel, um das Ticket zu entschlüsseln und den Sitzungsschlüssel zu extrahieren. Wenn der Server den Sitzungsschlüssel nicht mehr benötigt, wird der Schlüssel gelöscht.

Der Client muss nicht jedes Mal auf den KDC zugreifen, wenn er auf diesen speziellen Server zugreifen möchte. Tickets können wieder verwendet werden. Als Vorsichtsmaßnahme vor der Möglichkeit eines Ticket Diebstahls verfügen Tickets über eine Ablaufzeit, die durch die KDC in der Ticket Struktur angegeben wird. Wie lange ein Ticket gültig ist, hängt von der Kerberos-Richtlinie für den Bereich ab. Tickets sind in der Regel nicht länger als acht Stunden, sondern über die Länge einer normalen [*Anmelde Sitzung*](../secgloss/l-gly.md). Wenn sich der Benutzer auf einer Client Arbeitsstation abmeldet, wird der Cache des Client Tickets geleert, und alle Tickets und Client Sitzungsschlüssel werden zerstört.

 

 
