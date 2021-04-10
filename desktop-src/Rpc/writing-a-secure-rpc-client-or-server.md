---
title: Schreiben eines sicheren RPC-Clients oder-Servers
description: Dieser Abschnitt enthält Empfehlungen für bewährte Methoden zum Schreiben eines sicheren RPC-Clients oder-Servers.
ms.assetid: b738b780-247c-4108-b64d-0a4883895182
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, Schreiben eines sicheren Clients oder Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac006f82a0db8abcd7184b2453a970521004145b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039353"
---
# <a name="writing-a-secure-rpc-client-or-server"></a>Schreiben eines sicheren RPC-Clients oder-Servers

Dieser Abschnitt enthält Empfehlungen für bewährte Methoden zum Schreiben eines sicheren RPC-Clients oder-Servers.

Die Informationen in diesem Abschnitt gelten für Windows 2000 und Windows XP. Dieser Abschnitt gilt für alle Protokoll Sequenzen, einschließlich [**Ncalrpc**](/windows/desktop/Midl/ncalrpc). Entwickler sind tendenziell der Ansicht, dass **Ncalrpc** kein potenzielles Ziel für einen Angriff ist. Dies gilt nicht für einen Terminal Server, bei dem potenziell Hunderte von Benutzern Zugriff auf einen Dienst haben, und das kompromittieren oder sogar das herunter schalten eines diendienstanbieters kann dazu führen, dass zusätzlicher Zugriff möglich ist.

Dieser Abschnitt ist in die folgenden Themen unterteilt:

-   [Zu verwendende Sicherheitsanbieter](which-security-provider-to-use.md)
-   [Steuern der Client Authentifizierung](controlling-client-authentication.md)
-   [Auswählen einer Authentifizierungs Ebene](choosing-an-authentication-level.md)
-   [Auswählen von Sicherheits-QoS-Optionen](choosing-security-qos-options.md)
-   [Allgemeiner Fehler: die Annahme, dass rpcserverregisterauthinfo den Server nicht autorisiert](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [Rückrufe](callbacks.md)
-   [Null-Sitzungen](null-sessions.md)
-   [Verwenden des/robust-Flags](use-the-robust-flag.md)
-   [IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf](idl-techniques-for-better-interface-and-method-design.md)
-   [Strict-und typstrikte Kontext Handles](strict-and-type-strict-context-handles.md)
-   [Ihren Peer nicht als vertrauenswürdig einstufen](do-not-trust-your-peer.md)
-   [Endpunkt Sicherheit nicht verwenden](do-not-use-endpoint-security.md)
-   [Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [Überprüfen Sie, ob der Server, den er als](verify-the-server-is-who-it-claims-to-be.md)
-   [Verwenden von gängigen Protokoll Sequenzen](use-mainstream-protocol-sequences.md)
-   [Wie sicher ist jetzt der RPC-Server?](how-secure-is-my-rpc-server-now.md)

 

 