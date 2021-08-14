---
description: Das TLS-Handshakeprotokoll (Transport Layer Security) ist für die Authentifizierung und den Schlüsselaustausch verantwortlich, die zum Einrichten oder Fortsetzen sicherer Sitzungen erforderlich sind.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: TLS Handshake-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe32e11127bf46088aa04e58dd6444620cea327c08d2609e01749efcb1e00df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915818"
---
# <a name="tls-handshake-protocol"></a>TLS Handshake-Protokoll

Das TLS-Handshakeprotokoll [*(Transport Layer Security)*](../secgloss/t-gly.md) ist für die Authentifizierung und den Schlüsselaustausch verantwortlich, die zum Einrichten oder Fortsetzen sicherer Sitzungen erforderlich sind. Beim Einrichten einer sicheren [*Sitzung*](../secgloss/s-gly.md)verwaltet das Handshake-Protokoll Folgendes:

-   Verschlüsselungssammlungsaushandlung
-   Authentifizierung des Servers und optional des Clients
-   Austausch von Sitzungsschlüsselinformationen.

## <a name="cipher-suite-negotiation"></a>Cipher Suite-Aushandlung

Der Client und der Server nehmen Kontakt auf und wählen die Verschlüsselungssammlung aus, die während des gesamten Nachrichtenaustauschs verwendet wird.

## <a name="authentication"></a>Authentifizierung

In TLS bestätigt ein Server seine Identität gegenüber dem Client. Der Client muss möglicherweise auch seine Identität gegenüber dem Server nachweisen. PKI, die Verwendung von [*Paaren aus öffentlichem und privatem Schlüssel,*](../secgloss/p-gly.md)ist die Grundlage dieser Authentifizierung. Die genaue Methode, die für die Authentifizierung verwendet wird, wird durch die ausgehandelte Verschlüsselungssammlung bestimmt.

## <a name="key-exchange"></a>Key Exchange

Client und Server tauschen Zufallszahlen und eine spezielle Zahl namens Pre-Master Secret aus. Diese Zahlen werden mit zusätzlichen Daten kombiniert, mit denen Client und Server ihr gemeinsames Geheimnis erstellen können, das als Geheimer Hauptschlüssel bezeichnet wird. Der geheime Hauptschlüssel wird von Client und Server verwendet, um den Mac-Schreibschlüssel zu generieren. Dabei handelt es sich um den Sitzungsschlüssel, der für das [*Hashing*](../secgloss/h-gly.md)verwendet wird, und den Schreibschlüssel, bei dem es sich um den für die Verschlüsselung verwendeten [*Sitzungsschlüssel*](../secgloss/s-gly.md) handelt.

## <a name="establishing-a-secure-session-by-using-tls"></a>Einrichten einer sicheren Sitzung mit TLS

Das TLS Handshake-Protokoll umfasst die folgenden Schritte:

1.  Der Client sendet eine "Client hello"-Nachricht zusammen mit dem Zufallswert des Clients und unterstützten Verschlüsselungssammlungen an den Server.
2.  Der Server antwortet, indem er eine "Server hello"-Nachricht zusammen mit dem zufälligen Wert des Servers an den Client sendet.
3.  Der Server sendet sein Zertifikat zur Authentifizierung an den Client und kann ein Zertifikat vom Client anfordern. Der Server sendet die Meldung "Server hello done".
4.  Wenn der Server ein Zertifikat vom Client angefordert hat, sendet der Client es.
5.  Der Client erstellt ein zufälliges Pre-Master Secret und verschlüsselt es mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) aus dem Serverzertifikat und sendet den verschlüsselten Pre-Master Secret an den Server.
6.  Der Server empfängt den Geheimen Pre-Master-Schlüssel. Server und Client generieren jeweils den geheimen Hauptschlüssel und [*die Sitzungsschlüssel*](../secgloss/s-gly.md) basierend auf dem Geheimen Prähauptschlüssel.
7.  Der Client sendet die Benachrichtigung "Verschlüsselungsspezifikation ändern" an den Server, um anzugeben, dass der Client die neuen [*Sitzungsschlüssel*](../secgloss/s-gly.md) zum [*Hashen*](../secgloss/h-gly.md) und Verschlüsseln von Nachrichten verwendet. Der Client sendet auch die Meldung "Client abgeschlossen".
8.  Der Server empfängt "Verschlüsselungsspezifikation ändern" und schaltet den Sicherheitsstatus der Datensatzebene mithilfe der [*Sitzungsschlüssel*](../secgloss/s-gly.md)in [*symmetrische Verschlüsselung*](../secgloss/s-gly.md) um. Der Server sendet die Meldung "Server finished" an den Client.
9.  Client und Server können jetzt Anwendungsdaten über den gesicherten Kanal austauschen, den sie eingerichtet haben. Alle Nachrichten, die von Client zu Server und von Server zu Client gesendet werden, werden mithilfe des Sitzungsschlüssels verschlüsselt.

## <a name="resuming-a-secure-session-by-using-tls"></a>Fortsetzen einer sicheren Sitzung mit TLS

1.  Der Client sendet eine "Client hello"-Nachricht mithilfe der Sitzungs-ID der Sitzung, die fortgesetzt werden soll.
2.  Der Server überprüft seinen Sitzungscache auf eine übereinstimmende Sitzungs-ID. Wenn eine Übereinstimmung gefunden wird und der Server die Sitzung fortsetzen kann, sendet er eine "Server hello"-Nachricht mit der Sitzungs-ID.
    > [!Note]  
    > Wenn keine Übereinstimmung mit der Sitzungs-ID gefunden wird, generiert der Server eine neue Sitzungs-ID, und der TLS-Client und der Server führen einen vollständigen Handshake aus.

     

3.  Client und Server müssen Nachrichten vom Typ "Verschlüsselungsspezifikation ändern" austauschen und Nachrichten vom Typ "Client abgeschlossen" und "Server fertig" senden.
4.  Client und Server können nun den Austausch von Anwendungsdaten über den sicheren Kanal fortsetzen.

 

 
