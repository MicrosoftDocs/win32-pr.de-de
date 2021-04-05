---
title: Überprüfen Sie, ob der Server, den er als
description: Es empfiehlt sich, die gegenseitige Authentifizierung zu verwenden und so die Identität des Servers zu überprüfen.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710577"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="b1f9a-103">Überprüfen Sie, ob der Server, den er als</span><span class="sxs-lookup"><span data-stu-id="b1f9a-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="b1f9a-104">Es empfiehlt sich, die gegenseitige Authentifizierung zu verwenden und so die Identität des Servers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="b1f9a-105">Ein Beispiel für einen allgemeinen Fehler, bei dem dies nicht der Fall ist, sind Anwendungen mit einem lokalen Dienst, der von den Clients aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="b1f9a-106">In manchen Konfigurationen kann ein Administrator entscheiden, dass der Systemdienst nicht wirklich nützlich ist und ihn möglicherweise beendet.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="b1f9a-107">Ein erfinderischer Angreifer auf einem Terminal Server Computer kann einen Prozess starten, der auf demselben Endpunkt lauscht, und wenn ein Client eine Verbindung mit einem Endpunkt herstellt, sodass der Identitätswechsel auf dem Server ohne gegenseitige Authentifizierung des Servers möglich ist, kann der Angreifer die Identität des Clients annehmen und auf die Daten des Clients zugreifen oder im Auftrag des Clients Netzwerk Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="b1f9a-108">Die meisten Systemdienste werden unter einem bekannten Konto ausgeführt, z. b. "localsysyem", "LocalService" oder "Network Service", das mithilfe der gegenseitigen Authentifizierung überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="b1f9a-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




