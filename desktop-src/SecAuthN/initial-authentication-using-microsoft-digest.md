---
description: Die erste Authentifizierung erfolgt, wenn der Server eine Abfrageantwort von einem Client empfängt.
ms.assetid: 8a5cf26b-0b2a-4f19-807b-9ec4d533cdd4
title: Anfängliche Authentifizierung mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6e9582161eb43e5109af4dc223ae150e94cbddf9b3514dabcb30339a3acc36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482620"
---
# <a name="initial-authentication-using-microsoft-digest"></a>Anfängliche Authentifizierung mit Microsoft Digest

Die erste Authentifizierung erfolgt, wenn der Server eine Abfrageantwort von einem Client empfängt. Die Authentifizierung einer Abfrageantwort umfasst in der Regel mindestens zwei Server:

-   Der Ursprungsserver empfängt die Anforderung vom Client und gibt eine Abfrage aus und empfängt dann die Abfrageantwort vom Client, die authentifiziert werden muss.
-   Der authentifizierende Server empfängt Autorisierungsinformationen vom ursprünglichen Server und führt die Authentifizierung aus. Dieser Server ist in der Regel ein Domänencontroller, der mehrere Ursprungsserver unterstützt.

Wenn der ursprüngliche Server eine Anforderung mit einem Autorisierungsheader empfängt, der eine Digest-Abfrageantwort enthält, wird die Authentifizierung wie folgt fortgesetzt:

-   Die Identität des Ursprungsservers wird anhand des Servers überprüft, der in der Nonce der Abfrage codiert ist.
-   Der in der Nonce codierte Zeitstempel wird überprüft. Wenn die Nonce abgelaufen ist und die Benutzernamen-/Kennwortinformationen gültig sind, beendet der ursprüngliche Server die Authentifizierung, indem er eine neue Digest-Abfrage mit der veralteten Anweisung auf "true" ausgibt. Dies gibt an, dass nur die Nonce "veraltet" war und der Client auf die neue Abfrage mit dem Kennwort antworten kann, das er in der vorherigen Antwort verwendet hat. Wenn der Client nach dem Senden der Abfrageantwort für die veraltete Abfrage eine neue Abfrage empfängt, muss der Client eine neue Abfrageantwort generieren.
-   Wenn die Wiedergabeerkennung erzwungen wird, wird die nc-Direktive (Nonce-Anzahl) anhand der vom Server verwalteten Nonce-Sitzungsdatenbank überprüft.
-   Der authentifizierende Server wird identifiziert und die Autorisierungsinformationen des Clients gesendet.
-   Der authentifizierende Server überprüft die Identität des in der Nonce codierten Servers mit der Identität des Ursprungsservers.
-   Der authentifizierende Server, bei dem es sich um einen Domänencontroller handelt, ruft das Kennwort des Benutzers ab.
-   Mithilfe der Autorisierungsinformationen, des Kennworts und der Identifikation des Ursprungsservers berechnet der authentifizierende Server den Wert, den der Client in der Antwortdirektive der Abfrageantwort angegeben haben sollte. Der authentifizierende Server vergleicht den berechneten Wert mit der Antwort des Clients, um den Erfolg oder Fehler der Authentifizierung zu bestimmen.

Wenn die Authentifizierung erfolgreich ist, werden der [*Sicherheitskontext*](../secgloss/s-gly.md) des Benutzers und ein [*Digestsitzungsschlüssel*](../secgloss/s-gly.md) an den ursprünglichen Server zurückgegeben. Wenn die Authentifizierung fehlschlägt, muss der ursprüngliche Server eine Fehlerantwort generieren. Nach erfolgreicher Authentifizierung gibt der ursprüngliche Server die angeforderte Ressource an den Client zurück.

Der vom authentifizierenden Server zurückgegebene Digestsitzungsschlüssel wird vom Ursprungsserver zur Verwendung bei der Authentifizierung zukünftiger Anforderungen zwischengespeichert. Weitere Informationen finden Sie unter [Authentifizieren nachfolgender Anforderungen mit Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
