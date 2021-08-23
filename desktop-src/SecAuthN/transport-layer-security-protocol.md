---
description: Schannel unterstützt die Versionen 1.0, 1.1 und 1.2 des TLS-Protokolls (Transport Layer Security).
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: TLS-Protokoll (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed6bc76b6a491105607c3110cda32723bbba75fdf55abe97f7667f397060209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915592"
---
# <a name="transport-layer-security-protocol"></a>TLS-Protokoll (Transport Layer Security)

Schannel unterstützt die Versionen 1.0, 1.1 und 1.2 des [*tls-Protokolls (Transport Layer Security).*](../secgloss/t-gly.md) Dieses Protokoll ist ein Industriestandard, der auf den Datenschutz von Informationen ausgelegt ist, die über das Internet ausgetauscht werden. TLS geht davon aus, dass ein verbindungsorientierter Transport, in der Regel TCP, verwendet wird. Mit dem TLS-Protokoll können Client-/Serveranwendungen die folgenden Sicherheitsrisiken erkennen:

-   Manipulation von Nachrichten
-   Abfangen von Nachrichten
-   Nachrichtenfälschung

Die vollständige Spezifikation des TLS-Protokolls ist auf der IETF-Website verfügbar: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .

## <a name="organization-of-tls"></a>Organisation von TLS

Die folgenden Schritte sind an der Verwendung von TLS für die Client-/Serverkommunikation beteiligt:

 **So verwenden Sie TLS für die Client-/Serverkommunikation**

1.  Aushandlung von Handshake und Verschlüsselungssammlung
2.  Authentifizierung von Parteien
3.  Schlüsselbezogener Informationsaustausch
4.  Austausch von Anwendungsdaten

Die Schritte, aus denen TLS besteht, sind in zwei Protokolle unterteilt, die zusammen Verbindungssicherheit bieten:

-   [TLS Handshake-Protokoll](tls-handshake-protocol.md)– (Schritte 1 bis 3)
-   [TLS-Datensatzprotokoll](tls-record-protocol.md)– (Schritt 4)

## <a name="sspi-with-tls-implementations"></a>SSPI mit TLS-Implementierungen

Da TLS über keine GSSAPI-Spezifikation verfügt, sind TLS-Implementierer möglicherweise nicht mit den SSPI-Funktionen vertraut. Anwendungen rufen die SSPI-Funktionen auf, um verfügbare Pakete aufzuzählen, Handles für Anmeldeinformationen zu erstellen und mit ihnen zu arbeiten, Sicherheitskontexte zu erstellen und den Datenschutz der Nachrichtenintegrität sicherzustellen.

Um die SSPI-Funktionen zu unterstützen, die von Benutzermodusanwendungen verwendet werden, müssen die unter [Von SSP/APs im Benutzermodus implementierten](/windows/desktop/SecAuthN/authentication-functions) Funktionen aufgeführten Funktionen von TLS-Implementierungen wie schannel.dll unterstützt werden.

Ausführliche Informationen zu den SSPI-Funktionen und SSP-Funktionen finden Sie unter [Authentifizierungsfunktionen.](authentication-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TLS-Verschlüsselungssammlungen](tls-cipher-suites.md)
</dt> <dt>

[TLS im Vergleich zu SSL](tls-versus-ssl.md)
</dt> </dl>

 

 
