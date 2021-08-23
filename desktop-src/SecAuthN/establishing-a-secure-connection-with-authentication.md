---
description: In einem Client-/Serveranwendungsprotokoll wird ein Server an einen Kommunikationsport gebunden, z. B. an einen Socket oder eine RPC-Schnittstelle.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Herstellen einer sicheren Verbindung mit Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5f9458cf578481e049dcf2b41d6607b3c6151ce16a938cfe0e398ae7b3bf56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008248"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Herstellen einer sicheren Verbindung mit Authentifizierung

In einem [*Client-/Serveranwendungsprotokoll*](/windows/desktop/SecGloss/a-gly)wird ein Server an einen Kommunikationsport gebunden, z. B. an einen Socket oder eine RPC-Schnittstelle. Der Server wartet dann, bis ein Client eine Verbindung mit dem Dienst herstellen und den Dienst anfordern kann. Die Sicherheit beim Einrichten der Verbindung ist bei der gegenseitigen Authentifizierung zweifach:

-   Clientauthentifizierung durch den Server.
-   Serverauthentifizierung durch den Client.

Die Client- und Serverkomponenten einer [](/windows/desktop/SecGloss/s-gly) Transportanwendung verwenden ein Sicherheitspaket, um eine sichere Verbindung zum Übertragen von Nachrichten herzustellen. Der erste Schritt beim Herstellen einer sicheren Verbindung besteht im Erstellen eines [*Sicherheitskontexts.*](/windows/desktop/SecGloss/s-gly) das heißt, eine nicht transparente Datenstruktur, die die für eine [](/windows/desktop/SecGloss/s-gly) Verbindung relevanten Sicherheitsdaten enthält, z. B. einen Sitzungsschlüssel und die Dauer der Sitzung.

Ein Sicherheitskontext ist im Wesentlichen eine Nachricht aus dem Sicherheitspaket, das dem Client zugeordnet ist, an das Sicherheitspaket, das dem Server zugeordnet ist. Daher erfordert das Erstellen eines Sicherheitskontexts in der Regel, dass sowohl der Client als auch der Server Aufrufe an die jeweiligen Sicherheitspakete ausführen. Weitere Informationen zu Kontextfunktionen finden Sie unter [Kontextverwaltung.](authentication-functions.md)

Das Protokoll, das zum Herstellen einer sicheren, authentifizierten Verbindung verwendet wird, umfasst den Austausch von mindestens einem "Sicherheitstoken" zwischen dem Client und dem Server. Diese Token werden als nicht transparente Nachrichten von den [](/windows/desktop/SecGloss/a-gly)beiden Seiten zusammen mit anderen Anwendungsprotokoll-spezifischen Informationen gesendet. Als nicht transparente Nachricht wird das Token von einer Sicherheitspaketfunktion vom Client empfangen, die es nicht interpretieren oder ändern kann, und als Nachricht an den Server weitergeleitet. Das Token ist auch für den Server nicht transparent, was das Token weder interpretieren noch ändern kann. Der Server gibt das nicht transparente Token zur Interpretation an das Sicherheitspaket weiter. Das Paket informiert den Server dann über die Clientauthentifizierung oder den Fehler bei der Authentifizierung.

Der Client empfängt das Token des Servers in einer Nachricht, ruft das Token aus der empfangenen Nachricht ab und verwendet dieses Token in einem Aufruf des Sicherheitspakets. Der Client ruft dann das Sicherheitspaket erneut auf und gibt an, ob eine sichere Verbindung hergestellt wurde oder ob ein weiterer Austausch erforderlich ist, bevor eine sichere Verbindung hergestellt wird. Theoretisch gibt es keine Beschränkung für die Anzahl der erforderlichen Austausche von Sicherheitstoken. In der Praxis ist nur eine begrenzte Anzahl von Umtauschen erforderlich. Die NTLM-Authentifizierung basiert auf dem Abfrage-/Antwortschema und verwendet drei Authentisierungen, um einen Client beim Server zu authentifizieren. Das [*Kerberos-Protokoll*](/windows/desktop/SecGloss/k-gly) Version 5.0 kann zusätzlichen Nachrichtenaustausch erfordern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisierung des Clientkontexts](client-context-initialization.md)
</dt> <dt>

[Initialisierung des Serverkontexts](server-context-initialization.md)
</dt> </dl>

 

 
