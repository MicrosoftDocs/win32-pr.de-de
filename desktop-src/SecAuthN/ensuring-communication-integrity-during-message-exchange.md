---
description: Nachdem ein Sicherheitskontext eingerichtet wurde, kann die Anwendung die Nachrichtenunterstützungsfunktionen verwenden, um manipulationssichere Nachrichten zu übertragen.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Sicherstellen der Kommunikationsintegrität während Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394f78fcc1e5becf4bdfc7c67db52e1af177a7f3aa427d1c6182a080f0ae87bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008258"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Sicherstellen der Kommunikationsintegrität während Exchange

Nachdem ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eingerichtet wurde, kann die Anwendung die [Nachrichtenunterstützungsfunktionen](authentication-functions.md) verwenden, um manipulationssichere Nachrichten zu übertragen.

Der Client oder Server übergibt den Sicherheitskontext und eine Nachricht an die [**MakeSignature-Funktion,**](/windows/desktop/api/Sspi/nf-sspi-makesignature) um eine sichere Signatur zu generieren, die verhindert, dass die Nachricht während der Übertragung geändert wird. Der Empfänger der Nachricht ruft die [**VerifySignature-Funktion**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) auf. **VerifySignature** verwendet die Informationen in der Signatur, um zu überprüfen, ob die empfangene Nachricht während der Übertragung nicht geändert wurde. Der Client und der Server können auch verschlüsselte Nachrichten mit [**EncryptMessage (Allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (Allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)austauschen.

Der Server in einer authentifizierten Verbindung kann auch Verbindungen mit anderen Remotecomputern im Namen des Clients herstellen, nachdem [**impersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext)aufgerufen wurde.

 

 
