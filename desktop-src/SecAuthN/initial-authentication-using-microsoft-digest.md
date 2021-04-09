---
description: Die erste Authentifizierung findet statt, wenn der Server eine Abfrage Antwort von einem Client empfängt.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Anfängliche Authentifizierung mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed4960d947bbc60df962e6a9b71be755e158c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867860"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Anfängliche Authentifizierung mit Microsoft Digest

Die erste Authentifizierung findet statt, wenn der Server eine Abfrage Antwort von einem Client empfängt. Die Authentifizierung einer Challenge-Antwort umfasst in der Regel mindestens zwei Server:

-   Der Ursprungsserver – empfängt die Anforderung vom Client und gibt eine Herausforderung aus und empfängt dann die Anforderungs Antwort vom Client, die authentifiziert werden muss.
-   Der authentifizier Ende Server – empfängt Autorisierungs Informationen vom ursprünglichen Server und führt die Authentifizierung aus. Dieser Server ist in der Regel ein Domänen Controller, der mehrere Ursprungsserver unterstützt.

Wenn der Ursprungsserver eine Anforderung mit einem Autorisierungs Header empfängt, der eine digestaufforderungs-Antwort enthält, erfolgt die Authentifizierung wie folgt:

-   Die Identität des Ursprungs Servers wird anhand des Servers überprüft, der in der Nonce der Challenge codiert ist.
-   Der in der Nonce codierte Zeitstempel wird geprüft. Wenn die Nonce abgelaufen ist und die Benutzernamen-/Kennwortinformationen gültig sind, beendet der Ursprungsserver die Authentifizierung, indem er eine neue digestfrage ausgibt, bei der die veraltete Direktive auf "true" festgelegt ist. Dies deutet darauf hin, dass nur das Nonce-Element "veraltet" war, und der Client kann auf die neue Abfrage mit dem Kennwort reagieren, das in der vorherigen Antwort verwendet wurde. Wenn der Client nach dem Senden der Abfrage Antwort für die veraltete Herausforderung eine neue Herausforderung erhält, muss der Client eine neue Abfrage Antwort generieren.
-   Wenn die Wiedergabe Erkennung erzwungen wird, wird die NC-Direktive (Nonce count) anhand der Nonce-sitzungsdatenbank überprüft, die vom Server verwaltet wird.
-   Der authentifizier Ende Server wird identifiziert und sendet die Autorisierungs Informationen des Clients.
-   Der authentifizier Ende Server überprüft die Identität des Servers, der in der Nonce verschlüsselt ist, anhand der Identität des Ursprungs Servers.
-   Der authentifizier Ende Server, bei dem es sich um einen Domänen Controller handelt, ruft das Kennwort des Benutzers ab.
-   Mithilfe der Autorisierungs Informationen, des Kennworts und der Ursprungsserver Identifikation berechnet der authentifizier Ende Server den Wert, den der Client in der Response-Direktive der Abfrage Antwort bereitstellen sollte. Der authentifizier Ende Server vergleicht den berechneten Wert mit der Antwort des Clients, um zu ermitteln, ob die Authentifizierung erfolgreich war oder fehlgeschlagen ist.

Wenn die Authentifizierung erfolgreich ist, werden der [*Sicherheitskontext*](../secgloss/s-gly.md) des Benutzers und ein Digest- [*Sitzungsschlüssel*](../secgloss/s-gly.md) an den ursprünglichen Server zurückgegeben. Wenn die Authentifizierung fehlschlägt, muss der Ursprungsserver eine Fehler Antwort generieren. Nach erfolgreicher Authentifizierung gibt der Ursprungsserver die angeforderte Ressource an den Client zurück.

Der vom authentifizier enden Server zurückgegebene Digest-Sitzungsschlüssel wird vom Ursprungsserver für die Authentifizierung zukünftiger Anforderungen zwischengespeichert. Weitere Informationen finden Sie unter [Authentifizieren von nachfolgenden Anforderungen mit Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
