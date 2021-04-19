---
description: SChannel unterstützt die Versionen 1,0, 1,1 und 1,2 des Transport Layer Security (TLS)-Protokolls.
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: TLS-Protokoll (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364113"
---
# <a name="transport-layer-security-protocol"></a>TLS-Protokoll (Transport Layer Security)

SChannel unterstützt die Versionen 1,0, 1,1 und 1,2 des [*Transport Layer Security (TLS)-Protokolls*](../secgloss/t-gly.md). Dieses Protokoll ist ein Industriestandard, der den Schutz der über das Internet kommunizierten Informationen schützt. TLS geht davon aus, dass ein Verbindungs orientierter Transport (in der Regel TCP) verwendet wird. Das TLS-Protokoll ermöglicht es Client/Server-Anwendungen, die folgenden Sicherheitsrisiken zu erkennen:

-   Manipulation von Nachrichten
-   Abfangen der Nachricht
-   Nachrichten Fälschung

Die vollständige Spezifikation des TLS-Protokolls ist auf der IETF-Website verfügbar: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>TLS-Organisation

Die folgenden Schritte sind bei der Verwendung von TLS für die Client/Server-Kommunikation beteiligt:

 **So verwenden Sie TLS für die Client/Server-Kommunikation**

1.  Hand Shake-und Chiffre Suite-Aushandlung
2.  Authentifizierung von Parteien
3.  Schlüssel bezogener Informationsaustausch
4.  Anwendungsdaten Austausch

Die Schritte, die TLS bilden, sind in zwei Protokolle unterteilt, die zusammen die Verbindungssicherheit bereitstellen:

-   [TLS-Handshake-Protokoll](tls-handshake-protocol.md)– (Schritte 1 – 3)
-   [TLS-Daten Satz Protokoll](tls-record-protocol.md)– (Schritt 4)

## <a name="sspi-with-tls-implementations"></a>SSPI mit TLS-Implementierungen

Da TLS keine GSSAPI-Spezifikation hat, sind TLS-Implementierer möglicherweise nicht mit den SSPI-Funktionen vertraut. Anwendungen rufen die SSPI-Funktionen zum Auflisten verfügbarer Pakete, zum Erstellen und Bearbeiten von Handles für Anmelde Informationen, zum Erstellen von Sicherheits Kontexten und zum Schutz der Nachrichten Integrität auf.

Um die von Benutzermodusanwendungen verwendeten SSPI-Funktionen zu unterstützen, müssen die Funktionen, die in Funktionen aufgelistet sind, die [von SSP/APS im Benutzermodus implementiert](/windows/desktop/SecAuthN/authentication-functions) werden, von TLS-Implementierungen wie schannel.dll unterstützt werden.

Ausführliche Informationen zu den SSPI-Funktionen und SSP-Funktionen finden Sie unter [Authentifizierungsfunktionen](authentication-functions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TLS-Verschlüsselungs Sammlungen](tls-cipher-suites.md)
</dt> <dt>

[TLS und SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
