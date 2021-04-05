---
title: Endpunkt Sicherheit nicht verwenden
description: Endpoint Security ist ein Sicherheitsmodell, bei dem eine Sicherheits Beschreibung angegeben wird, wenn ein Endpunkt mit der RpcServerUseProtseq \-Gruppe von RPC-Funktionen erstellt wird.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709960"
---
# <a name="do-not-use-endpoint-security"></a><span data-ttu-id="b09bf-103">Endpunkt Sicherheit nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="b09bf-103">Do Not Use Endpoint Security</span></span>

<span data-ttu-id="b09bf-104">Endpoint Security ist ein Sicherheitsmodell, bei dem eine Sicherheits Beschreibung angegeben wird, wenn ein Endpunkt mit der [**rpcserveruseprotabq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) - \* Gruppe der RPC-Funktionen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b09bf-104">Endpoint security is a security model in which a security descriptor is given when an endpoint is created with the [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq)\* group of RPC functions.</span></span> <span data-ttu-id="b09bf-105">Verwenden Sie dieses Sicherheitsmodell nicht.</span><span class="sxs-lookup"><span data-stu-id="b09bf-105">Do not use this security model.</span></span> <span data-ttu-id="b09bf-106">Weisen Sie diesen Funktionen keine Sicherheits Beschreibungen zu.</span><span class="sxs-lookup"><span data-stu-id="b09bf-106">Do not give security descriptors to those functions.</span></span> <span data-ttu-id="b09bf-107">Diese Methode ist am besten eine Verschwendung von CPU-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="b09bf-107">At best, this method is a waste of CPU resources.</span></span> <span data-ttu-id="b09bf-108">Im schlimmsten Fall kann es in vielen Umgebungen vorkommen, dass die Sicherheits Beschreibung umgangen werden kann, da die auf [anderen RPC-Endpunkten, die im gleichen Prozessabschnitt ausgeführt werden](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) , ein Blick darauf hat.</span><span class="sxs-lookup"><span data-stu-id="b09bf-108">At worst, in many environments it is possible to circumvent the security descriptor, as the [Be Wary of Other RPC Endpoints Running In the Same Process](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) section exemplifies.</span></span>

<span data-ttu-id="b09bf-109">Die Endpunkt Sicherheit ist nur aus Gründen der Abwärtskompatibilität vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b09bf-109">Endpoint security exists only for backward compatibility.</span></span>

 

 




