---
title: Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.
description: Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711573"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a><span data-ttu-id="4e713-103">Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e713-103">Be Wary of Other RPC Endpoints Running in the Same Process</span></span>

<span data-ttu-id="4e713-104">Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen.</span><span class="sxs-lookup"><span data-stu-id="4e713-104">When an application resides in a process with other RPC servers, all applications listen on all protocols.</span></span> <span data-ttu-id="4e713-105">Wenn eine Komponente z. b. [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* nur für LRPC aufruft, ist nicht notwendigerweise nur über LRPC zugänglich.</span><span class="sxs-lookup"><span data-stu-id="4e713-105">As such, if a component calls [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* for LRPC only, it is not necessarily accessible over LRPC only.</span></span> <span data-ttu-id="4e713-106">Möglicherweise ist über andere Protokolle darauf zugegriffen werden, da andere RPC-Server im Prozess möglicherweise an Pipes oder Sockets lauschen (z. b.).</span><span class="sxs-lookup"><span data-stu-id="4e713-106">It may be accessible over other protocols, since other RPC servers in the process may be listening on pipes or sockets (for example).</span></span>

<span data-ttu-id="4e713-107">Ähnlich wie bei strengen Kontext Handles bedeutet das Platzieren eines anderen Endpunkts im Prozess nicht, dass kein anderer Endpunkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4e713-107">Similar to strict context handles, not putting another endpoint in the process does not mean another endpoint does not exist.</span></span> <span data-ttu-id="4e713-108">Unabhängig davon, wie Sie den Server registrieren, gibt es keine besondere Zuordnung zwischen Ihrer Schnittstelle und dem Endpunkt. alle Schnittstellen können für alle Endpunkte in diesem Prozess aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4e713-108">Regardless of how you register your server, there is no special association between your interface and your endpoint; all interfaces are callable on all endpoints in that process.</span></span> <span data-ttu-id="4e713-109">Dies ist ein weiterer Grund, warum das Endpunkt Sicherheitsmodell nicht wirksam ist. Wenn eine Sicherheits Beschreibung für einen Endpunkt platziert wird, können Angreifer die-Schnittstelle auf einem anderen Endpunkt abrufen.</span><span class="sxs-lookup"><span data-stu-id="4e713-109">This is another reason why the endpoint security model is ineffective; if a security descriptor is placed on an endpoint, attackers can call the interface on another endpoint.</span></span>

<span data-ttu-id="4e713-110">Um sicherzustellen, dass ein Prozess nur für eine bestimmte Protokoll Sequenz aufgerufen wird, registrieren Sie eine Sicherheits Rückruffunktion, und überprüfen Sie in dieser Funktion, welche Protokoll Sequenz der Aufruf durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="4e713-110">To ensure a process be called only on a specific protocol sequence, register a security callback function, and in that function, check on which protocol sequence the call is made.</span></span>

 

 




