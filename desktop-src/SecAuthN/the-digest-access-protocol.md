---
description: Das Digest-Zugriffsprotokoll
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: Das Digest-Zugriffsprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86aa8f05580c27c866c0568dbc67c4d5ba5c2016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557663"
---
# <a name="the-digest-access-protocol"></a>Das Digest-Zugriffsprotokoll

Das von [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) angegebene Digest-Zugriffsprotokoll wird von der Microsoft Digest [*Security Support Provider*](../secgloss/s-gly.md) (SSP) implementiert. Die-Implementierung besteht aus einer Reihe von Sicherheitskontext Funktionen von [Microsoft Security Support Provider Interface](sspi.md) (SSPI), die von Client-/Serveranwendungen aufgerufen werden:

-   Einrichten eines [*Sicherheits Kontexts*](../secgloss/s-gly.md) für den Nachrichtenaustausch.
-   Abrufen von Datenobjekten, die vom Digest-SSP benötigt werden, z. b. [*Anmelde*](../secgloss/c-gly.md) Informationen und Kontext Handles.
-   Zugriffs Mechanismen für die Nachrichten [*Integrität*](../secgloss/i-gly.md) und-Vertraulichkeit.

Die Digest-Zugriffs Authentifizierung erfolgt innerhalb von gekoppelten Anforderungs-/Antwort-Transaktionen mit Anforderungen, die auf dem Client und den auf dem Server ursprünglichen Antworten liegen. Für eine erfolgreiche Digest-Zugriffs Authentifizierung sind zwei Anforderungs-/Antwort-Paare erforderlich.

Wenn der Digest-SSP für die HTTP-Authentifizierung verwendet wird, besteht keine Verbindung zwischen dem ersten und dem zweiten Anforderungs-/Antwort-Paar. Das heißt, der Server wartet nicht auf die zweite Anforderung, nachdem die erste Antwort gesendet wurde.

In der folgenden Abbildung werden die Schritte beschrieben, die für den HTTP-Pfad von einem Client und Server ausgeführt werden, um eine Authentifizierung mit dem Digest-SSP abzuschließen. Der SASL-Mechanismus nutzt die gegenseitige Authentifizierung, sodass die Authentifizierungsdaten beim letzten ASC-Server-Rückruf an den Client zurückgesendet werden, der überprüft, ob der Client mit dem richtigen Server kommuniziert.

![Digest-Zugriffsprotokoll](images/digest1.png)

Der Prozess beginnt mit dem Client, der vom Server eine durch den Zugriff geschützte Ressource anfordert, indem er die HTTP-Anforderung 1 sendet.

Der Server empfängt die HTTP-Anforderung 1 und ermittelt, dass die Ressource Authentifizierungsinformationen erfordert, die nicht in der Anforderung enthalten waren. Der Server generiert eine Herausforderung für den Client wie folgt:

1.  Der Server erhält seine [*Anmelde*](../secgloss/c-gly.md) Informationen, indem er die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufruft.
2.  Der Server generiert die Digestherausforderung durch Aufrufen der Funktion " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) ".
3.  Der Server sendet einen WWW-Authenticate-Header als Antwort auf die Anforderung des Clients (als HTTP-Antwort 1 angezeigt). Der-Header enthält die Digestherausforderung und eine nicht transparente-Direktive, die einen Verweis auf einen für den Client festgelegten partiellen [*Sicherheitskontext*](../secgloss/s-gly.md) enthält. Der-Header wird mit einem 401-Statuscode gesendet, der angibt, dass die Client Anforderung einen nicht autorisierten Zugriffsfehler generiert hat. Weitere Informationen zur Digestherausforderung finden Sie unter [Inhalt einer](contents-of-a-digest-challenge.md) digestaufforderung und [Erstellen der Digestherausforderung](generating-the-digest-challenge.md).
4.  Der Client empfängt die HTTP-Antwort 1, extrahiert die vom Server gesendete Digest-Abfrage und generiert wie folgt eine digestaufforderungs-Antwort:
    1.  Die Anmelde Informationen des Benutzers werden abgerufen, indem die [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) -Funktion aufgerufen oder der Benutzer interaktiv zur Eingabe von Anmelde Informationen aufgefordert wird.
    2.  Die Informationen und Anmelde Informationen werden an die [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion übergeben, die die digestaufforderungs-Antwort generiert.
5.  Der Client sendet einen Autorisierungs Header, der die Abfrage Antwort an den Server enthält (angezeigt als HTTP-Anforderung 2). Weitere Informationen zur digestaufforderungs-Antwort finden Sie unter [Inhalt einer digestaufforderungs](contents-of-a-digest-challenge-response.md) -Antwort und [Erstellen der Digest](generating-the-digest-challenge-response.md)-Abfrage Antwort.
6.  Der Server empfängt die HTTP-Anforderung 2, extrahiert die vom Client gesendete Abfrage Antwort und authentifiziert die Informationen durch Aufrufen der Funktion " [**akzeptsecuritycontext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) ". Ausführliche Informationen zum Authentifizierungsprozess finden Sie unter [erste Authentifizierung mit Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  Der Server sendet HTTP-Antwort 2 als zweite und letzte Antwort an den Client zurück, die für das Digest-Zugriffsprotokoll erforderlich ist. Wenn die Authentifizierung erfolgreich ist, enthält diese Antwort die angeforderte Ressource.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Inhalt einer digestaufforderungs-Antwort](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
