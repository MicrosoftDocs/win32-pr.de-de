---
description: Erläutert, wie Nachrichten mithilfe von Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Schützen von Nachrichten mit Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab0add351287b6c90cfe0781151c0378da56f309214b03ed12d1325a6e55d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920739"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Schützen von Nachrichten mit Microsoft Digest

## <a name="http-and-sasl"></a>HTTP und SASL

Um bestimmte Arten von Sicherheitsverstößen zu erkennen, verwenden Client und Server die [](../secgloss/i-gly.md) Nachrichtenintegritätsfunktionen [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) des Sicherheitsunterstützungsanbieters (Security [Support Provider Interface,](sspi.md) SSPI), um Nachrichten zu schützen.

Ein Client ruft die [**MakeSignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-makesignature) auf, um eine Nachricht mithilfe des [*Sicherheitskontexts zu signieren.*](../secgloss/s-gly.md) Der Server verwendet die [**VerifySignature-Funktion,**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) um den Ursprung der Nachricht zu überprüfen. Zusätzlich zur Überprüfung [](../secgloss/d-gly.md) der Signatur, die die Nachricht begleitet, überprüft die **VerifySignature-Funktion** auch, ob die [*Nonce-Anzahl*](../secgloss/n-gly.md) (durch die nc-Direktive angegeben) um eins größer als die letzte Anzahl ist, die für die Nonce gesendet wurde. Wenn dies nicht der Fall ist, gibt die **VerifySignature-Funktion** einen SEC \_ OUT OF \_ \_ SEQUENCE-Fehlercode zurück.

## <a name="sasl-only"></a>Nur SASL

Die [**Funktionen EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) gewährleisten Vertraulichkeit für Nachrichten nach der Authentifizierung, die zwischen Client und Server ausgetauscht werden.

Um die Nachrichten vertraulichkeitsfunktionen verwenden zu können, müssen der Server und der Client einen [*Sicherheitskontext*](../secgloss/s-gly.md) mit den folgenden Attributen eingerichtet haben:

-   Die durch die qop-Direktive angegebene Qualität des Schutzes muss "auth-conf" sein.
-   Ein Verschlüsselungsmechanismus muss mit der Cipher-Direktive angegeben worden sein.

 

 
