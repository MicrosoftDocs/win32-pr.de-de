---
description: Das TLS-Handshake-Protokoll (Transport Layer Security) ist für die Authentifizierung und den Schlüsselaustausch zuständig, die erforderlich sind, um sichere Sitzungen einzurichten oder fortzusetzen.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: TLS-Handshake-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350022"
---
# <a name="tls-handshake-protocol"></a>TLS-Handshake-Protokoll

Das TLS-Handshake-Protokoll ( [*Transport Layer Security*](../secgloss/t-gly.md) ) ist für die Authentifizierung und den Schlüsselaustausch zuständig, die erforderlich sind, um sichere Sitzungen einzurichten oder fortzusetzen. Beim Einrichten einer sicheren [*Sitzung*](../secgloss/s-gly.md)verwaltet das Handshake-Protokoll Folgendes:

-   Cipher Suite-Aushandlung
-   Authentifizierung des Servers und optional des Clients
-   Informationsaustausch für Sitzungsschlüssel.

## <a name="cipher-suite-negotiation"></a>Cipher Suite-Aushandlung

Der Client und der Server stellen eine Verbindung her und wählen die Verschlüsselungs Sammlung aus, die im gesamten Nachrichtenaustausch verwendet werden soll.

## <a name="authentication"></a>Authentifizierung

In TLS weist ein Server seine Identität dem Client zu. Außerdem muss der Client seine Identität möglicherweise dem Server nachweisen. PKI, die Verwendung von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md), ist die Grundlage für diese Authentifizierung. Die genaue Methode, die für die Authentifizierung verwendet wird, wird von der ausgehandelten Chiffre Sammlung bestimmt.

## <a name="key-exchange"></a>Schlüsselaustausch

Der Client und der Server tauschen Zufallszahlen und eine besondere Zahl aus, die als geheimer Hauptschlüssel bezeichnet wird. Diese Zahlen werden mit zusätzlichen Daten kombiniert, sodass Client und Server ihren gemeinsamen geheimen Schlüssel erstellen können, der als geheimer Hauptschlüssel bezeichnet wird. Der geheime Hauptschlüssel wird von Client und Server verwendet, um den geheimen Lese Schlüssel zu generieren. Dies ist der für das [*Hashwert*](../secgloss/h-gly.md)verwendete Sitzungsschlüssel und der Schlüssel zum Schreiben, bei dem es sich um den [*Sitzungsschlüssel*](../secgloss/s-gly.md) handelt, der für die Verschlüsselung verwendet wird.

## <a name="establishing-a-secure-session-by-using-tls"></a>Einrichten einer sicheren Sitzung mithilfe von TLS

Das TLS-Handshake-Protokoll umfasst die folgenden Schritte:

1.  Der Client sendet eine "Client Hello"-Meldung sowie den Zufallswert und die unterstützten Verschlüsselungs Sammlungen des Clients an den Server.
2.  Der Server antwortet, indem er eine "Server Hello"-Meldung zusammen mit dem zufälligen Wert des Servers an den Client sendet.
3.  Der Server sendet sein Zertifikat zur Authentifizierung an den Client und fordert möglicherweise ein Zertifikat vom Client an. Der Server sendet die Meldung "Server Hello Done".
4.  Wenn der Server ein Zertifikat vom Client angefordert hat, sendet der Client es.
5.  Der Client erstellt einen zufälligen geheimen Hauptschlüssel und verschlüsselt ihn mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) aus dem Zertifikat des Servers, wobei der verschlüsselte geheime Hauptschlüssel an den Server gesendet wird.
6.  Der Server empfängt den geheimen Hauptschlüssel. Der Server und der Client generieren jeweils den geheimen Haupt [*Schlüssel und die Sitzungsschlüssel*](../secgloss/s-gly.md) basierend auf dem geheimen Hauptschlüssel.
7.  Der Client sendet eine Benachrichtigung vom Typ "Verschlüsselungs Spezifikation ändern" an den Server, um anzugeben, dass der Client die neuen [*Sitzungsschlüssel*](../secgloss/s-gly.md) für das [*hashten*](../secgloss/h-gly.md) und Verschlüsseln von Nachrichten verwendet. Der Client sendet außerdem die Meldung "der Client wurde beendet".
8.  Der Server empfängt "Verschlüsselungs Spezifikation ändern" und schaltet seinen Sicherheitsstatus auf Datensatzebene mithilfe der [*Sitzungsschlüssel*](../secgloss/s-gly.md)in die [*symmetrische Verschlüsselung*](../secgloss/s-gly.md) ein. Der Server sendet die Meldung "der Server wurde beendet" an den Client.
9.  Client und Server können nun Anwendungsdaten über den gesicherten Kanal austauschen, den Sie eingerichtet haben. Alle vom Client an den Server und vom Server an den Client gesendeten Nachrichten werden mit dem Sitzungsschlüssel verschlüsselt.

## <a name="resuming-a-secure-session-by-using-tls"></a>Fortsetzen einer sicheren Sitzung mithilfe von TLS

1.  Der Client sendet eine "Client Hello"-Meldung mithilfe der Sitzungs-ID der Sitzung, die fortgesetzt werden soll.
2.  Der Server überprüft seinen Sitzungs Cache auf eine passende Sitzungs-ID. Wenn eine Entsprechung gefunden wird und der Server die Sitzung fortsetzen kann, sendet er eine "Server Hello"-Meldung mit der Sitzungs-ID.
    > [!Note]  
    > Wenn keine Sitzungs-ID gefunden wird, generiert der Server eine neue Sitzungs-ID, und der TLS-Client und-Server führen einen vollständigen Handshake aus.

     

3.  Client und Server müssen die Nachrichten "Änderung der Verschlüsselungs Spezifikation" austauschen und "Client wurde beendet" und "Server beendet" senden.
4.  Client und Server können nun den Anwendungsdaten Austausch über den sicheren Kanal fortsetzen.

 

 
