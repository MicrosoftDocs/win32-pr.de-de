---
description: Erläutert, wie Nachrichten mithilfe von Microsoft Digest geschützt werden.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Schützen von Nachrichten mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362544"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Schützen von Nachrichten mit Microsoft Digest

## <a name="http-and-sasl"></a>HTTP und SASL

Um bestimmte Arten von Sicherheitsverletzungen zu erkennen, verwenden der Client und der Server die SSPI ( [Security Support Provider Interface](sspi.md) )-Nachrichten [*Integritäts*](../secgloss/i-gly.md) Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) zum Schützen von Nachrichten.

Ein Client ruft die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion auf, um eine Nachricht mithilfe Ihres [*Sicherheits Kontexts*](../secgloss/s-gly.md)zu signieren. Der Server verwendet die [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktion, um den Ursprung der Nachricht zu überprüfen. Zusätzlich zur Überprüfung der [*Signatur*](../secgloss/d-gly.md) , die die Nachricht begleitet, prüft die **VerifySignature** -Funktion auch, ob die [*Nonce*](../secgloss/n-gly.md) -Anzahl (angegeben durch die NC-Direktive) eine höhere als die letzte für die Nonce gesendete Anzahl ist. Wenn dies nicht der Fall ist, gibt die **VerifySignature** -Funktion einen SEK \_ . aus dem Sequenz- \_ \_ Fehlercode zurück.

## <a name="sasl-only"></a>Nur SASL

Die Funktionen [**verschlüsseltmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) geben Vertraulichkeit für Nachrichten nach der Authentifizierung zwischen Client und Server an.

Um die Nachrichten Vertraulichkeits Funktionen zu verwenden, muss der Server und der Client einen [*Sicherheitskontext*](../secgloss/s-gly.md) mit den folgenden Attributen eingerichtet haben:

-   Die von der QoP-Direktive angegebene Qualität des Schutzes muss "auth-conf" lauten.
-   Ein Verschlüsselungsmechanismus muss mithilfe der Chiffre Direktive angegeben werden.

 

 
