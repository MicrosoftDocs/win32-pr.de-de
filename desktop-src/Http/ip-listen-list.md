---
title: IP-Abhörliste
description: Die HTTP-Server-APIs werden nicht an IP-Adressen und TCP-Port Paare gebunden, bis ein Benutzer ein URLPrefix registriert.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948040"
---
# <a name="ip-listen-list"></a><span data-ttu-id="b07f4-103">IP-Abhörliste</span><span class="sxs-lookup"><span data-stu-id="b07f4-103">IP Listen List</span></span>

<span data-ttu-id="b07f4-104">Die HTTP-Server-APIs werden nicht an IP-Adressen und TCP-Port Paare gebunden, bis ein Benutzer ein URLPrefix registriert.</span><span class="sxs-lookup"><span data-stu-id="b07f4-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="b07f4-105">Wenn eine Registrierung in der Anforderungs Warteschlange eingegeben wird, bindet die HTTP-Server-API standardmäßig eine Bindung an den Port, der im URLPrefix (z. b. Port 80) für alle \_ \_ auf dem Computer verfügbaren IP-Adressen (inaddr any oder INADDR6 any) angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b07f4-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="b07f4-106">Probleme treten auf, wenn Anwendungen von Drittanbietern (nicht die HTTP-Server-APIs) an die IP-Adresse und die Port 80-Paare auf dem Computer gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b07f4-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="b07f4-107">Die HTTP-Server-API bietet eine Möglichkeit zum Konfigurieren der Liste der IP-Adressen, die Sie bindet, und löst dieses Koexistenzproblem.</span><span class="sxs-lookup"><span data-stu-id="b07f4-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="b07f4-108">Der Systemadministrator Ruft die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion auf, wobei der Parameter *ConfigID* auf den Wert httpserviceconmegiplistenlist festgelegt ist, um die IP-Abhörliste anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b07f4-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="b07f4-109">Der Liste können sowohl IPv4-als auch IPv6-Adressen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b07f4-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="b07f4-110">Die eingegebenen IP-Adressen gelten für alle Anwendungen auf dem Computer, die die HTTP-Server-API verwenden und über die Neustarts des Computers hinweg beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="b07f4-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="b07f4-111">Alle Änderungen an der Konfiguration der IP-Abhörliste werden jedoch nicht dynamisch durchgeführt. in den meisten Fällen ist möglicherweise ein Systemneustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b07f4-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




