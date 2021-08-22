---
description: Das Digestzugriffsprotokoll
ms.assetid: 7b2fd75e-dd0d-4a63-a84b-a64f08f883f2
title: Das Digestzugriffsprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45fea65fc25df87ef434e7bfea5cb81690cdc06f82b72882438fe4475a1895b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916433"
---
# <a name="the-digest-access-protocol"></a>Das Digestzugriffsprotokoll

Das von [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt) angegebene Digestzugriffsprotokoll wird vom Microsoft Digest [*Security Support Provider*](../secgloss/s-gly.md) (SSP) implementiert. Die Implementierung besteht aus einer Reihe von Sicherheitskontextfunktionen der [Microsoft Security Support Provider Interface](sspi.md) (SSPI), die Client-/Serveranwendungen aufrufen:

-   Richten Sie einen [*Sicherheitskontext*](../secgloss/s-gly.md) für den Nachrichtenaustausch ein.
-   Rufen Sie datenobjekte ab, die vom Digest-SSP benötigt werden, z. B. [*Anmeldeinformationen*](../secgloss/c-gly.md) und Kontexthandles.
-   Zugreifen auf [*nachrichtenintegritäts-*](../secgloss/i-gly.md) und vertraulichkeitsmechanismen.

Die Digestzugriffsauthentifizierung erfolgt in gekoppelten Anforderungs-/Antworttransaktionen, wobei Anforderungen vom Client und Antworten vom Server stammen. Für eine erfolgreiche Digestzugriffsauthentifizierung sind zwei Anforderungs-Antwort-Paare erforderlich.

Wenn der Digest-SSP für die HTTP-Authentifizierung verwendet wird, wird keine Verbindung zwischen dem ersten und zweiten Anforderungs-/Antwortpaar hergestellt. Anders ausgedrückt: Der Server wartet nach dem Senden der ersten Antwort nicht auf die zweite Anforderung.

Die folgende Abbildung zeigt die Schritte, die ein Client und ein Server auf dem HTTP-Pfad ausführen, um eine Authentifizierung mit dem Digest-SSP abzuschließen. Der SASL-Mechanismus nutzt die gegenseitige Authentifizierung, sodass Authentifizierungsdaten beim letzten ASC-Serveraufruf an den Client zurückgesandt werden, der überprüft, ob der Client mit dem richtigen Server kommuniziert.

![Digestzugriffsprotokoll](images/digest1.png)

Der Prozess beginnt damit, dass der Client eine zugriffsgeschützte Ressource vom Server anfordert, indem er HTTP-Anforderung 1 sendet.

Der Server empfängt HTTP-Anforderung 1 und ermittelt, dass die Ressource Authentifizierungsinformationen erfordert, die nicht in der Anforderung enthalten waren. Der Server generiert eine Herausforderung für den Client wie folgt:

1.  Der Server ruft seine [*Anmeldeinformationen*](../secgloss/c-gly.md) ab, indem er die [**AcquireCredentialsHandle-Funktion aufruft.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)
2.  Der Server generiert die Digest-Abfrage, indem er die [**AcceptSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) aufruft.
3.  Der Server sendet einen WWW-Authenticate-Header als Antwort auf die Anforderung des Clients (als HTTP-Antwort 1 angezeigt). Der Header enthält die Digest-Abfrage und eine nicht transparente Direktive, die einen Verweis auf einen für den Client eingerichteten partiellen [*Sicherheitskontext*](../secgloss/s-gly.md) enthält. Der Header wird mit dem Statuscode 401 gesendet, der angibt, dass die Clientanforderung einen Fehler aufgrund eines nicht autorisierten Zugriffs generiert hat. Weitere Informationen zur Digest-Herausforderung finden Sie unter [Inhalt einer Digest-Herausforderung](contents-of-a-digest-challenge.md) und [Generieren der Digest-Herausforderung.](generating-the-digest-challenge.md)
4.  Der Client empfängt HTTP-Antwort 1, extrahiert die vom Server gesendete Digest-Abfrage und generiert wie folgt eine Digest-Abfrageantwort:
    1.  Die Anmeldeinformationen des Benutzers werden entweder durch Aufrufen der [**AcquireCredentialsHandle-Funktion**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) oder durch interaktives Auffordern des Benutzers zur Eingabe von Anmeldeinformationen abgerufen.
    2.  Die Informationen zur Abfrage und zu den Anmeldeinformationen werden an die [**InitializeSecurityContext (General)-Funktion**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) übergeben, die die Digest-Abfrageantwort generiert.
5.  Der Client sendet einen Autorisierungsheader, der die Abfrageantwort an den Server enthält (als HTTP-Anforderung 2 dargestellt). Weitere Informationen zur Antwort auf die Digest-Abfrage finden Sie unter [Inhalt einer Digest-Abfrageantwort](contents-of-a-digest-challenge-response.md) und [Generieren der Digest-Abfrageantwort.](generating-the-digest-challenge-response.md)
6.  Der Server empfängt HTTP-Anforderung 2, extrahiert die vom Client gesendete Abfrageantwort und authentifiziert die Informationen durch Aufrufen der [**AcceptSecurityContext (General)-Funktion.**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Ausführliche Informationen zum Authentifizierungsprozess finden Sie unter [Erste Authentifizierung mit Microsoft Digest](initial-authentication-using-microsoft-digest.md).
7.  Der Server sendet HTTP-Antwort 2 als zweite und letzte Antwort, die vom Digestzugriffsprotokoll benötigt wird, zurück an den Client. Wenn die Authentifizierung erfolgreich ist, enthält diese Antwort die angeforderte Ressource.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Inhalt einer Digest-Abfrageantwort](contents-of-a-digest-challenge-response.md)
</dt> </dl>

 

 
