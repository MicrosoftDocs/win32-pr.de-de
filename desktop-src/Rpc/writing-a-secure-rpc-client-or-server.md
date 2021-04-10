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
# <a name="writing-a-secure-rpc-client-or-server"></a><span data-ttu-id="fd209-104">Schreiben eines sicheren RPC-Clients oder-Servers</span><span class="sxs-lookup"><span data-stu-id="fd209-104">Writing a Secure RPC Client or Server</span></span>

<span data-ttu-id="fd209-105">Dieser Abschnitt enthält Empfehlungen für bewährte Methoden zum Schreiben eines sicheren RPC-Clients oder-Servers.</span><span class="sxs-lookup"><span data-stu-id="fd209-105">This section provides best practice recommendations for writing a secure RPC client or server.</span></span>

<span data-ttu-id="fd209-106">Die Informationen in diesem Abschnitt gelten für Windows 2000 und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd209-106">The information in this section applies to Windows 2000 and Windows XP.</span></span> <span data-ttu-id="fd209-107">Dieser Abschnitt gilt für alle Protokoll Sequenzen, einschließlich [**Ncalrpc**](/windows/desktop/Midl/ncalrpc).</span><span class="sxs-lookup"><span data-stu-id="fd209-107">This section applies to all protocol sequences, including [**ncalrpc**](/windows/desktop/Midl/ncalrpc).</span></span> <span data-ttu-id="fd209-108">Entwickler sind tendenziell der Ansicht, dass **Ncalrpc** kein potenzielles Ziel für einen Angriff ist. Dies gilt nicht für einen Terminal Server, bei dem potenziell Hunderte von Benutzern Zugriff auf einen Dienst haben, und das kompromittieren oder sogar das herunter schalten eines diendienstanbieters kann dazu führen, dass zusätzlicher Zugriff möglich ist.</span><span class="sxs-lookup"><span data-stu-id="fd209-108">Developers tend to think **ncalrpc** is not a probable target for an attack, which is not true on a terminal server where potentially hundreds of users have access to a service, and compromising or even bringing down a service can lead to acquiring extra access.</span></span>

<span data-ttu-id="fd209-109">Dieser Abschnitt ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="fd209-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="fd209-110">Zu verwendende Sicherheitsanbieter</span><span class="sxs-lookup"><span data-stu-id="fd209-110">Which Security Provider To Use</span></span>](which-security-provider-to-use.md)
-   [<span data-ttu-id="fd209-111">Steuern der Client Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="fd209-111">Controlling Client Authentication</span></span>](controlling-client-authentication.md)
-   [<span data-ttu-id="fd209-112">Auswählen einer Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="fd209-112">Choosing an Authentication Level</span></span>](choosing-an-authentication-level.md)
-   [<span data-ttu-id="fd209-113">Auswählen von Sicherheits-QoS-Optionen</span><span class="sxs-lookup"><span data-stu-id="fd209-113">Choosing Security QOS Options</span></span>](choosing-security-qos-options.md)
-   [<span data-ttu-id="fd209-114">Allgemeiner Fehler: die Annahme, dass rpcserverregisterauthinfo den Server nicht autorisiert</span><span class="sxs-lookup"><span data-stu-id="fd209-114">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>](common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server.md)
-   [<span data-ttu-id="fd209-115">Rückrufe</span><span class="sxs-lookup"><span data-stu-id="fd209-115">Callbacks</span></span>](callbacks.md)
-   [<span data-ttu-id="fd209-116">Null-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="fd209-116">Null Sessions</span></span>](null-sessions.md)
-   [<span data-ttu-id="fd209-117">Verwenden des/robust-Flags</span><span class="sxs-lookup"><span data-stu-id="fd209-117">Use the /robust Flag</span></span>](use-the-robust-flag.md)
-   [<span data-ttu-id="fd209-118">IDL-Techniken für einen besseren Schnittstellen-und Methoden Entwurf</span><span class="sxs-lookup"><span data-stu-id="fd209-118">IDL Techniques for Better Interface and Method Design</span></span>](idl-techniques-for-better-interface-and-method-design.md)
-   [<span data-ttu-id="fd209-119">Strict-und typstrikte Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="fd209-119">Strict and Type Strict Context Handles</span></span>](strict-and-type-strict-context-handles.md)
-   [<span data-ttu-id="fd209-120">Ihren Peer nicht als vertrauenswürdig einstufen</span><span class="sxs-lookup"><span data-stu-id="fd209-120">Do Not Trust Your Peer</span></span>](do-not-trust-your-peer.md)
-   [<span data-ttu-id="fd209-121">Endpunkt Sicherheit nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="fd209-121">Do Not Use Endpoint Security</span></span>](do-not-use-endpoint-security.md)
-   [<span data-ttu-id="fd209-122">Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd209-122">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md)
-   [<span data-ttu-id="fd209-123">Überprüfen Sie, ob der Server, den er als</span><span class="sxs-lookup"><span data-stu-id="fd209-123">Verify The Server Is Who It Claims To Be</span></span>](verify-the-server-is-who-it-claims-to-be.md)
-   [<span data-ttu-id="fd209-124">Verwenden von gängigen Protokoll Sequenzen</span><span class="sxs-lookup"><span data-stu-id="fd209-124">Use Mainstream Protocol Sequences</span></span>](use-mainstream-protocol-sequences.md)
-   [<span data-ttu-id="fd209-125">Wie sicher ist jetzt der RPC-Server?</span><span class="sxs-lookup"><span data-stu-id="fd209-125">How Secure is my RPC Server Now?</span></span>](how-secure-is-my-rpc-server-now.md)

 

 