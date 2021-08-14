---
description: Die anfängliche Authentifizierung erfolgt, wenn der Server eine Antwort auf eine Herausforderung von einem Client empfängt.
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

Die anfängliche Authentifizierung erfolgt, wenn der Server eine Antwort auf eine Herausforderung von einem Client empfängt. Die Authentifizierung einer Antwort auf eine Herausforderung umfasst in der Regel mindestens zwei Server:

-   Der Ursprungsserver empfängt die Anforderung vom Client und gibt eine Aufforderung aus und empfängt dann die Antwort vom Client, die authentifiziert werden muss.
-   Der authentifizierende Server empfängt Autorisierungsinformationen vom Ursprungsserver und führt die Authentifizierung aus. Dieser Server ist in der Regel ein Domänencontroller, der mehrere Ursprungsserver unterstützt.

Wenn der Ursprungsserver eine Anforderung mit einem Autorisierungsheader empfängt, der eine Digest-Challenge-Antwort enthält, wird die Authentifizierung wie folgt fortgesetzt:

-   Die Identität des Ursprungsservers wird anhand des Servers überprüft, der in der Nonce der Herausforderung codiert ist.
-   Der in der Nonce codierte Zeitstempel wird überprüft. Wenn die Nonce abgelaufen ist und die Benutzernamen-/Kennwortinformationen gültig sind, beendet der Ursprungsserver die Authentifizierung, indem er eine neue Digest-Herausforderung ausstellen, bei der die veraltete -Direktive auf "true" festgelegt ist. Dies gibt an, dass nur die Nonce "veraltet" war und der Client auf die neue Herausforderung mit dem Kennwort reagieren kann, das er in der vorherigen Antwort verwendet hat. Wenn der Client nach dem Senden der Antwort auf die Herausforderung für die veraltete Herausforderung eine neue Herausforderung empfängt, muss der Client eine neue Antwort auf die Herausforderung generieren.
-   Wenn die Wiedergabeerkennung erzwungen wird, wird die NC-Direktive (Nonce-Anzahl) mit der nonce-Sitzungsdatenbank überprüft, die vom Server verwaltet wird.
-   Der authentifizierende Server wird identifiziert und sendet die Autorisierungsinformationen des Clients.
-   Der authentifizierende Server überprüft die Identität des Servers, der in der Nonce codiert ist, anhand der Identität des Ursprungsservers.
-   Der authentifizierende Server, bei dem es sich um einen Domänencontroller handelt, ruft das Kennwort des Benutzers ab.
-   Mithilfe der Autorisierungsinformationen, des Kennworts und der Identifizierung des Ursprungsservers berechnet der authentifizierende Server den Wert, den der Client in der Antwortrichtlinie der Antwort der Herausforderung angegeben haben soll. Der authentifizierende Server vergleicht den berechneten Wert mit der Antwort des Clients, um den Erfolg oder Fehler der Authentifizierung zu ermitteln.

Wenn die Authentifizierung erfolgreich [](../secgloss/s-gly.md) ist, werden der Sicherheitskontext des Benutzers und ein [*Digestsitzungsschlüssel*](../secgloss/s-gly.md) an den Ursprungsserver zurückgegeben. Wenn bei der Authentifizierung ein Fehler auftritt, muss der Ursprungsserver eine Fehlerantwort generieren. Nach einer erfolgreichen Authentifizierung gibt der Ursprungsserver die angeforderte Ressource an den Client zurück.

Der vom authentifizierenden Server zurückgegebene Digestsitzungsschlüssel wird vom Ursprungsserver zur Authentifizierung zukünftiger Anforderungen zwischengespeichert. Weitere Informationen finden Sie unter [Authentifizieren nachfolgender Anforderungen mithilfe Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

 

 
