---
title: Entladen eines Servers mit ausstehenden Kontext Handles
description: Normalerweise war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontext Handles verarbeitet, ohne den Hostingprozess zu beenden, problematisch.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207280"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="39fae-103">Entladen eines Servers mit ausstehenden Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="39fae-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="39fae-104">Normalerweise war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontext Handles verarbeitet, ohne den Hostingprozess zu beenden, problematisch.</span><span class="sxs-lookup"><span data-stu-id="39fae-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="39fae-105">Dies liegt daran, dass die Lauf Zeit Routine nicht mehr gültig ist, wenn die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="39fae-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="39fae-106">Wenn ein Client mit einem zuvor geöffneten Kontext Handle fehlschlägt und die RPC-Laufzeit versucht, das Kontext Handle zu schließen, verstößt der Versuch, den Zugriff auf die Lauf Zeit Routine aufzurufen, und der Server stürzt ab.</span><span class="sxs-lookup"><span data-stu-id="39fae-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="39fae-107">Ab Windows XP wurde eine neue API mit dem Namen " [**rpcserverunregisterifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="39fae-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="39fae-108">**Rpcserverunregisterifex** schließt Kontext Handles, die von der Schnittstelle geöffnet werden, deren Registrierung aufgehoben wird. die Funktion [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39fae-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="39fae-109">Die Verwendung von **rpcserverunregisterifex** ist nicht erforderlich, wenn der gesamte Prozess heruntergefahren wird. Dies ist jedoch notwendig, wenn mindestens eine DLLs, die die Lauf Zeit Routinen gehostet, entladen wird, während ausstehende Kontext Handles vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="39fae-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




