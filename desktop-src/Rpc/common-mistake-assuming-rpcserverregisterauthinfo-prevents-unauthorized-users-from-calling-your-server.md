---
title: Häufige Fehler bei der Annahme, dass rpcserverregisterauthinfo das Aufrufen Ihres Servers durch nicht autorisierte Benutzer verhindert.
description: Wenn Sicherheitsanbieter auf dem Server mit der rpcserverregisterauthinfo-Funktion registriert werden, wird eine Option hinzugefügt, keine Anforderung.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713338"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a><span data-ttu-id="9617d-103">Allgemeiner Fehler: die Annahme, dass rpcserverregisterauthinfo den Server nicht autorisiert</span><span class="sxs-lookup"><span data-stu-id="9617d-103">Common Mistake: Assuming RpcServerRegisterAuthInfo Prevents Unauthorized Users from Calling your Server</span></span>

<span data-ttu-id="9617d-104">Wenn Sicherheitsanbieter auf dem Server mit der [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion registriert werden, wird eine Option hinzugefügt, keine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9617d-104">When security providers are registered on the server with the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function, an option is added, not a requirement.</span></span> <span data-ttu-id="9617d-105">Dies bedeutet, dass vorherige Registrierungen mit **rpcserverregisterauthinfo** nicht ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9617d-105">This means previous registrations with **RpcServerRegisterAuthInfo** are not replaced.</span></span> <span data-ttu-id="9617d-106">Dies bedeutet auch, dass nicht authentifizierte Clients weiterhin eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="9617d-106">This also means unauthenticated clients still can connect.</span></span> <span data-ttu-id="9617d-107">Durch Aufrufen der **rpcserverregisterauthinfo** -Funktion ist es nicht zulässig, dass nicht authentifizierte Clients eine Verbindung herstellen. Sie können zwar eine Verbindung herstellen, aber Funktionsaufrufe wie [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) können nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9617d-107">By calling the **RpcServerRegisterAuthInfo** function, unauthenticated clients are not disallowed from connecting; they can still connect, but function calls such as [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) will fail.</span></span> <span data-ttu-id="9617d-108">Wenn also die **rpcserverregisterauthinfo** -Funktion aufgerufen wird, sind potenzielle Angreifer nicht mehr vorhanden – vielmehr können Clients, die Zugriff haben sollen, Ihre Identität nachweisen.</span><span class="sxs-lookup"><span data-stu-id="9617d-108">So when the **RpcServerRegisterAuthInfo** function is called, potential attackers have not been weeded out—rather, clients that ought to have access are given a chance to prove their identity.</span></span> <span data-ttu-id="9617d-109">Überprüfungen müssen immer noch vorhanden sein, um zu bestimmen, ob potenzielle Angreifer versuchen, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9617d-109">Checks must still be in place to determine whether potential attackers are attempting to connect.</span></span>

 

 




