---
description: Nachdem ein Sicherheitskontext eingerichtet wurde, kann die Anwendung die Nachrichten Unterstützungsfunktionen verwenden, um Manipulations geschützte Nachrichten zu übertragen.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128805"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a>Sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs

Nachdem ein [*Sicherheitskontext*](/windows/desktop/SecGloss/s-gly) eingerichtet wurde, kann die Anwendung die [Nachrichten Unterstützungs](authentication-functions.md) Funktionen verwenden, um Manipulations geschützte Nachrichten zu übertragen.

Der Client oder Server übergibt den Sicherheitskontext und eine Meldung an die [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion, um eine sichere Signatur zu generieren, die verhindert, dass die Nachricht während der Übertragung geändert wird. Der Empfänger der Nachricht Ruft die [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) -Funktion auf. **VerifySignature** verwendet die Informationen in der Signatur, um sicherzustellen, dass die empfangene Nachricht während der Übertragung nicht geändert wurde. Der Client und der Server können verschlüsselte Nachrichten auch mit [**verschlüsselungsmessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) und [**DecryptMessage (allgemein)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)austauschen.

Der Server in einer authentifizierten Verbindung kann auch Verbindungen mit anderen Remote Computern im Namen des Clients nach [**dem Aufruf von**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext)"Identitätsnachweis Nachweis" herstellen.

 

 
