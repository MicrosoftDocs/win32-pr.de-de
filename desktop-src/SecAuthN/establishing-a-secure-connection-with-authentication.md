---
description: In einem Client/Server-Anwendungsprotokoll bindet ein Server an einen Kommunikationsport, z. b. einen Socket oder eine RPC-Schnittstelle.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Einrichten einer sicheren Verbindung mit der Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353907"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Einrichten einer sicheren Verbindung mit der Authentifizierung

In einem Client/Server- [*Anwendungsprotokoll*](/windows/desktop/SecGloss/a-gly)bindet ein Server an einen Kommunikationsport, z. b. einen Socket oder eine RPC-Schnittstelle. Der Server wartet dann darauf, dass ein Client eine Verbindung herstellt und den Dienst anfordert. Die Rolle der Sicherheit beim Einrichten der Verbindung erfolgt im Fall einer gegenseitigen Authentifizierung aus zwei Fällen:

-   Client Authentifizierung durch den Server.
-   Server Authentifizierung durch den Client.

Die Client-und Serverkomponenten einer Transport Anwendung verwenden ein [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) zum Herstellen einer sicheren Verbindung zum Übertragen von Nachrichten. Der erste Schritt beim Einrichten einer sicheren Verbindung besteht darin, einen [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly)zu erstellen. Das heißt, eine nicht transparente Datenstruktur, die die für eine Verbindung relevanten Sicherheitsdaten enthält, z. b. einen [*Sitzungsschlüssel*](/windows/desktop/SecGloss/s-gly) und die Dauer der Sitzung.

Bei einem Sicherheitskontext handelt es sich im Wesentlichen um eine Meldung von dem Sicherheitspaket, das dem Client zugeordnet ist, mit dem dem Server zugeordneten Sicherheitspaket. Folglich erfordert das Erstellen eines Sicherheits Kontexts in der Regel, dass sowohl der Client als auch der Server Aufrufe an die entsprechenden Sicherheitspakete durchführen. Weitere Informationen zu Kontextfunktionen finden Sie unter [Context Management (Kontext Verwaltung](authentication-functions.md)).

Das Protokoll, das zum Einrichten einer sicheren, authentifizierten Verbindung verwendet wird, umfasst den Austausch von einem oder mehreren "Sicherheits Token" zwischen dem Client und dem Server. Diese Token werden von den beiden Seiten als nicht transparente Nachrichten zusammen mit anderen [*Anwendungsprotokoll*](/windows/desktop/SecGloss/a-gly)spezifischen Informationen gesendet. Als nicht transparente Nachricht wird das Token von einer Sicherheitspaket Funktion vom Client empfangen, die es nicht interpretieren oder ändern kann und als Nachricht an den Server weitergeleitet wird. Das Token ist auch für den Server nicht transparent, wodurch das Token weder interpretiert noch geändert werden kann. Der Server leitet das nicht transparente Token zur Interpretation an das Sicherheitspaket weiter. Das Paket informiert den Server dann über die Client Authentifizierung oder den Fehler bei der Authentifizierung.

Der Client empfängt das Token des Servers in einer Nachricht, ruft das Token von der empfangenen Nachricht ab und verwendet dieses Token in einem aufgerufenen Sicherheitspaket. Der Client ruft dann das Sicherheitspaket erneut auf, um anzugeben, ob eine sichere Verbindung hergestellt wurde oder ob weitere Austausch Vorgänge erforderlich sind, bevor eine sichere Verbindung bereit ist. Theoretisch gibt es keine Beschränkung für die Anzahl der erforderlichen Austausch Vorgänge für Sicherheits Token. In der Praxis ist nur eine begrenzte Anzahl von Austausch Vorgängen erforderlich. Die NTLM-Authentifizierung basiert auf dem Challenge/Response-Schema und verwendet drei Beine zum Authentifizieren eines Clients beim Server. Das [*Kerberos*](/windows/desktop/SecGloss/k-gly) -Protokoll, Version 5,0, kann zusätzlichen Nachrichtenaustausch erfordern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client kontextinitialisierung](client-context-initialization.md)
</dt> <dt>

[Initialisierung des Server Kontexts](server-context-initialization.md)
</dt> </dl>

 

 
