---
title: Schreiben eines sicheren RPC-Clients oder -Servers
description: Dieser Abschnitt enthält Empfehlungen zu bewährten Methoden zum Schreiben eines sicheren RPC-Clients oder -Servers.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Remoteprozeduraufruf RPC , bewährte Methoden, Schreiben eines sicheren Clients oder Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b752d8dab216691105e428833c83bce28b974f121ddcc77861fbb6671d72dd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010388"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Schreiben eines sicheren RPC-Clients oder -Servers

Dieser Abschnitt enthält Empfehlungen zu bewährten Methoden zum Schreiben eines sicheren RPC-Clients oder -Servers.

Die Informationen in diesem Abschnitt gelten für Windows 2000 und Windows XP. Dieser Abschnitt gilt für alle Protokollsequenzen, einschließlich [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Entwickler sind tendenziell der Meinung, dass **ncalrpc** kein wahrscheinliches Ziel für einen Angriff ist. Dies gilt nicht für einen Terminalserver, auf dem potenziell Hunderte von Benutzern Zugriff auf einen Dienst haben, und das Kompromittieren oder sogar das Herunterskalieren eines Diensts kann zu zusätzlichem Zugriff führen.

Dieser Abschnitt ist in die folgenden Themen unterteilt:

-   [Welcher Sicherheitsanbieter verwendet werden soll](which-security-provider-to-use.md)
-   [Steuern der Clientauthentifizierung](controlling-client-authentication.md)
-   [Auswählen einer Authentifizierungsebene](choosing-an-authentication-level.md)
-   [Auswählen von QOS-Sicherheitsoptionen](choosing-security-qos-options.md)
-   [Allgemeiner Fehler: Angenommen, rpcServerRegisterAuthInfo verhindert, dass nicht autorisierte Benutzer Ihren Server aufrufen](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Rückrufe](callbacks.md)
-   [NULL-Sitzungen](null-sessions.md)
-   [Verwenden des Flags /robust](use-the-robust-flag.md)
-   [IDL-Techniken für einen besseren Schnittstellen- und Methodenentwurf](idl-techniques-for-better-interface-and-method-design.md)
-   [Strict- und Type Strict-Kontexthandles](strict-and-type-strict-context-handles.md)
-   [Ihrem Peer nicht vertrauen](do-not-trust-your-peer.md)
-   [Endpunktsicherheit nicht verwenden](do-not-use-endpoint-security.md)
-   [Seien Sie vorsichtig bei anderen RPC-Endpunkten, die im gleichen Prozess ausgeführt werden](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Vergewissern Sie sich, dass der Server Wer sein soll.](verify-the-server-is-who-it-claims-to-be.md)
-   [Verwenden von Standardprotokollsequenzen](use-mainstream-protocol-sequences.md)
-   [Wie sicher ist mein RPC-Server jetzt?](how-secure-is-my-rpc-server-now.md)

 

 